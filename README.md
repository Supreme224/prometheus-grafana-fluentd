Установка:
Скопировать репозиторий на нужную ВМ:

git clone https://github.com/Supreme224/prometheus-grafana-fluentd.git

Установить Ansible и Docker-Compose, если еще не были установлены:
sudo apt update
sudo apt install ansible docker-compose -y

Запустить плейбук

ansible-playbook playbook.yml


Grafana будет доступна http://<VM_IP>:3000 (default login: admin/admin)

Fluentd сохраняет логи в /var/log/test/

Описание метрик:

fluentd_status_buffer_queue_length Текущее количество чанков в очереди буфера.
fluentd_status_buffer_total_bytes Общий размер в байтах всех буферизованных данных по всем плагинам.
fluentd_status_retry_count Текущее Количество попыток повторной отправки для неудачных операций.
fluentd_status_buffer_newest_timekey Наиболее недавний временной ключ (timestamp) событий в буфере.
fluentd_status_buffer_oldest_timekey Наиболее старый временной ключ (timestamp) событий в буфере.
fluentd_output_status_retry_count Количество попыток повторной отправки специально для плагинов вывода.
fluentd_output_status_num_errors Общее количество ошибок, возникших в плагинах вывода.
fluentd_output_status_emit_count Количество операций emit (успешных эмиссий логов), выполненных плагинами вывода.
fluentd_output_status_retry_wait Текущее время ожидания перед следующей попыткой повторной отправки.
fluentd_output_status_emit_records Количество записей, успешно эмиттированных плагинами вывода, отражая объем обработанных данных.
fluentd_output_status_write_count Количество операций записи, выполненных плагинами вывода.
fluentd_output_status_rollback_count Количество операций rollback в плагинах вывода.
fluentd_output_status_flush_time_count Общее время, затраченное на операции flush в плагинах вывода.
fluentd_output_status_slow_flush_count Количество операций flush в плагинах вывода.
fluentd_output_status_buffer_total_bytes Общий размер в байтах буфера, используемого плагинами вывода, помогая в управлении ёмкостью буфера.
fluentd_output_status_buffer_stage_length Длина (количество чанков) в staging-области буфера для плагинов вывода.
fluentd_output_status_buffer_stage_byte_size Общий размер в байтах staging-области буфера для плагинов вывода.
fluentd_output_status_buffer_queue_length Текущая длина очереди в буфере для плагинов вывода.
fluentd_output_status_buffer_queue_byte_size Общий размер в байтах очереди в буфере для плагинов вывода.
fluentd_output_status_buffer_newest_timekey Наиболее новый временной ключ событий в буфере для плагинов вывода.
fluentd_output_status_buffer_oldest_timekey Наиболее старый временной ключ событий в буфере для плагинов вывода.
fluentd_output_status_buffer_available_space_ratio Соотношение доступного пространства в буфере для плагинов вывода, выраженное в процентах.