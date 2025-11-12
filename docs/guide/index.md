import { motion } from 'framer-motion';
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";

export default function BoardingSchoolPage() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-blue-50 to-blue-100 text-gray-800">
      {/* Header */}
      <header className="relative text-center bg-blue-700 text-white py-8 shadow-lg overflow-hidden">
        <img
          src="https://treemvietnam.net.vn/wp-content/uploads/2024/02/truong-thpt-dtnt-ntrang-long-488.jpg"
          alt="Logo Trường THPT DTNT Nơ Trang Long"
          className="mx-auto w-28 h-28 rounded-full shadow-md relative z-10"
        />
        <motion.h1
          className="text-3xl font-bold mt-4 relative z-10"
          initial={{ y: -20, opacity: 0 }}
          animate={{ y: 0, opacity: 1 }}
        >
          Trường THPT DTNT Nơ Trang Long - Đắk Lắk
        </motion.h1>
        <p className="italic mt-1 text-blue-100 relative z-10">Nơi học tập – Rèn luyện – Trưởng thành</p>
        <motion.div
          className="absolute inset-0 bg-cover bg-center opacity-20"
          style={{ backgroundImage: 'url(https://i.imgur.com/N4Y2RZQ.jpg)' }}
          initial={{ opacity: 0 }}
          animate={{ opacity: 0.2 }}
          transition={{ duration: 2 }}
        />
      </header>

      {/* Navigation */}
      <nav className="flex flex-wrap justify-center bg-blue-800 text-white">
        {['Trang chủ', 'Chương trình học', 'Cuộc sống nội trú', 'Giáo viên & Học sinh', 'Liên hệ'].map((item, i) => (
          <a key={i} href="#" className="px-6 py-3 hover:bg-blue-600 transition-all">{item}</a>
        ))}
      </nav>

      {/* Intro Section */}
      <section className="max-w-5xl mx-auto my-10 text-center px-4">
        <motion.h2 className="text-2xl font-semibold text-blue-800 mb-4"
          initial={{ opacity: 0, y: 20 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}>
          Chào mừng đến với Trường THPT DTNT Nơ Trang Long!
        </motion.h2>
        <p className="text-lg leading-relaxed">
          Trường THPT Dân tộc Nội trú Nơ Trang Long là nơi học sinh các dân tộc tỉnh Đắk Lắk cùng nhau học tập, rèn luyện và trưởng thành.
          Với sứ mệnh xây dựng môi trường học tập thân thiện, sáng tạo và phát triển toàn diện, ngôi trường là niềm tự hào của biết bao thế hệ.
        </p>
        <div className="mt-6">
          <Button asChild>
            <a href="https://treemvietnam.net.vn/truong-hoc-hanh-phuc/truong-thpt-dtnt-ntrang-long-488.html" target="_blank">
              Xem trang chính thức của trường
            </a>
          </Button>
        </div>
      </section>

      {/* Highlight Section */}
      <section className="max-w-6xl mx-auto px-6 grid md:grid-cols-3 gap-6 mb-12">
        {[
          {
            title: 'Phòng học hiện đại',
            text: 'Hệ thống phòng học khang trang, thiết bị đầy đủ giúp học sinh tiếp cận tri thức hiệu quả và sinh động.',
          },
          {
            title: 'Hoạt động ngoại khóa',
            text: 'Các câu lạc bộ thể thao, nghệ thuật và kỹ năng sống giúp học sinh phát huy năng khiếu và tinh thần đoàn kết.',
          },
          {
            title: 'Đời sống nội trú',
            text: 'Môi trường gắn kết, ấm áp như ngôi nhà thứ hai – nơi học sinh học cách sẻ chia và tự lập.',
          },
        ].map((card, i) => (
          <motion.div key={i} whileHover={{ scale: 1.03 }}>
            <Card className="shadow-lg hover:shadow-xl transition-all bg-white/80">
              <CardContent className="p-6 text-center">
                <h3 className="text-xl font-semibold text-blue-700 mb-3">{card.title}</h3>
                <p>{card.text}</p>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      {/* Photo Gallery */}
      <section className="max-w-6xl mx-auto mb-12 px-6 text-center">
        <motion.h2 className="text-2xl font-semibold text-blue-800 mb-6"
          initial={{ opacity: 0, y: 20 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}>
          Thư viện ảnh hoạt động học sinh
        </motion.h2>
        <div className="grid md:grid-cols-3 gap-4">
          {[
            'https://i.imgur.com/GV7U5J3.jpg',
            'https://i.imgur.com/tDuzRNy.jpg',
            'https://i.imgur.com/kz6D0KH.jpg',
            'https://i.imgur.com/3TPXx1B.jpg',
            'https://i.imgur.com/dm5x8uC.jpg',
            'https://i.imgur.com/9FnOqtr.jpg'
          ].map((url, i) => (
            <motion.img
              key={i}
              src={url}
              alt={`Ảnh hoạt động ${i + 1}`}
              className="rounded-lg shadow-md hover:shadow-xl transition-all h-56 w-full object-cover"
              whileHover={{ scale: 1.05 }}
            />
          ))}
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-blue-700 text-white text-center py-6">
        <p>&copy; 2025 Trường THPT DTNT Nơ Trang Long - Tỉnh Đắk Lắk</p>
        <p className="italic text-blue-100">Thành viên thực hiện: Vi Ngọc Anh, Lisia Eban</p>
      </footer>
    </div>
  );
}






