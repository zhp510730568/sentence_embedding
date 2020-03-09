# sentence_embedding
本项目基于bert实现了skip-thought思想的sentence embedding学习网络：
'''
export CUDA_VISIBLE_DEVICES=2,3,1
export BERT_BASE_DIR=../bert-as-language-model/model/chinese_L-12_H-768_A-12

nohup python3 -u src/model/sentence_embedding.py --do_train=true --do_predict=true --do_eval=true  --data_dir=./resources/ --vocab_file=$BERT_BASE_DIR/vocab.txt --bert_config_file=$BERT_BASE_DIR/bert_config.json   --init_checkpoint=$BERT_BASE_DIR/bert_model.ckpt --max_seq_length=100 --train_batch_size=4 --learning_rate=1e-4 --num_train_epochs=3 --output_dir=./resources/model_20190903 --warmup_proportion=0.1 --eval_batch_size=3 &
'''
