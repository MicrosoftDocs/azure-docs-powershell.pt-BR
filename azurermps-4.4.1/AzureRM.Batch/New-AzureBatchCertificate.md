---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611008"
---
# <span data-ttu-id="6e11a-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6e11a-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="6e11a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e11a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e11a-103">Adiciona um certificado à conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="6e11a-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e11a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e11a-104">SYNTAX</span></span>

### <span data-ttu-id="6e11a-105">Arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e11a-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e11a-106">RawData</span><span class="sxs-lookup"><span data-stu-id="6e11a-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e11a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e11a-107">DESCRIPTION</span></span>
<span data-ttu-id="6e11a-108">O cmdlet **New-AzureBatchCertificate** adiciona um certificado à conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="6e11a-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="6e11a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e11a-109">EXAMPLES</span></span>

### <span data-ttu-id="6e11a-110">Exemplo 1: adicionar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="6e11a-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="6e11a-111">Esse comando adiciona um certificado à conta em lotes especificada usando o arquivo E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="6e11a-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="6e11a-112">Exemplo 2: adicionar um certificado de dados brutos</span><span class="sxs-lookup"><span data-stu-id="6e11a-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="6e11a-113">O primeiro comando lê os dados do arquivo chamado MyCert. pfx na variável $RawData.</span><span class="sxs-lookup"><span data-stu-id="6e11a-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="6e11a-114">O segundo comando adiciona um certificado à conta em lotes especificada usando os dados brutos armazenados em $RawData.</span><span class="sxs-lookup"><span data-stu-id="6e11a-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="6e11a-115">OS</span><span class="sxs-lookup"><span data-stu-id="6e11a-115">PARAMETERS</span></span>

### <span data-ttu-id="6e11a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e11a-116">-BatchContext</span></span>
<span data-ttu-id="6e11a-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6e11a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e11a-118">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="6e11a-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e11a-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="6e11a-119">-FilePath</span></span>
<span data-ttu-id="6e11a-120">Especifica o caminho do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="6e11a-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="6e11a-121">O arquivo de certificado deve estar em um formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="6e11a-121">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e11a-122">-Senha</span><span class="sxs-lookup"><span data-stu-id="6e11a-122">-Password</span></span>
<span data-ttu-id="6e11a-123">Especifica a senha para acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="6e11a-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="6e11a-124">Você deve especificar esse parâmetro se especificar um certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="6e11a-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e11a-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="6e11a-125">-RawData</span></span>
<span data-ttu-id="6e11a-126">Especifica os dados brutos do certificado em formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="6e11a-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e11a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e11a-127">-DefaultProfile</span></span>
<span data-ttu-id="6e11a-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e11a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e11a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e11a-129">CommonParameters</span></span>
<span data-ttu-id="6e11a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e11a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e11a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e11a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e11a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e11a-132">INPUTS</span></span>

### <span data-ttu-id="6e11a-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e11a-133">BatchAccountContext</span></span>
<span data-ttu-id="6e11a-134">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6e11a-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6e11a-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="6e11a-135">Byte[]</span></span>
<span data-ttu-id="6e11a-136">O parâmetro ' RawData ' aceita o valor do tipo ' byte [] ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6e11a-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="6e11a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e11a-137">OUTPUTS</span></span>

## <span data-ttu-id="6e11a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e11a-138">NOTES</span></span>

## <span data-ttu-id="6e11a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e11a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6e11a-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6e11a-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="6e11a-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6e11a-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6e11a-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6e11a-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="6e11a-143">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="6e11a-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


