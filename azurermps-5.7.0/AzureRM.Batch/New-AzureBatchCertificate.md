---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441353"
---
# <span data-ttu-id="e5fb4-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e5fb4-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="e5fb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fb4-103">Adiciona um certificado à conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5fb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5fb4-104">SYNTAX</span></span>

### <span data-ttu-id="e5fb4-105">Arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="e5fb4-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5fb4-106">RawData</span><span class="sxs-lookup"><span data-stu-id="e5fb4-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5fb4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="e5fb4-108">O cmdlet **New-AzureBatchCertificate** adiciona um certificado à conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="e5fb4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="e5fb4-110">Exemplo 1: adicionar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="e5fb4-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="e5fb4-111">Esse comando adiciona um certificado à conta em lotes especificada usando o arquivo E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="e5fb4-112">Exemplo 2: adicionar um certificado de dados brutos</span><span class="sxs-lookup"><span data-stu-id="e5fb4-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="e5fb4-113">O primeiro comando lê os dados do arquivo chamado MyCert. pfx na variável $RawData.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="e5fb4-114">O segundo comando adiciona um certificado à conta em lotes especificada usando os dados brutos armazenados em $RawData.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="e5fb4-115">OS</span><span class="sxs-lookup"><span data-stu-id="e5fb4-115">PARAMETERS</span></span>

### <span data-ttu-id="e5fb4-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e5fb4-116">-BatchContext</span></span>
<span data-ttu-id="e5fb4-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e5fb4-118">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e5fb4-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e5fb4-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e5fb4-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5fb4-122">-DefaultProfile</span></span>
<span data-ttu-id="e5fb4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e5fb4-124">-FilePath</span></span>
<span data-ttu-id="e5fb4-125">Especifica o caminho do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="e5fb4-126">O arquivo de certificado deve estar em um formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="e5fb4-127">-Password</span></span>
<span data-ttu-id="e5fb4-128">Especifica a senha para acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="e5fb4-129">Você deve especificar esse parâmetro se especificar um certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="e5fb4-130">-RawData</span></span>
<span data-ttu-id="e5fb4-131">Especifica os dados brutos do certificado em formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5fb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fb4-132">CommonParameters</span></span>
<span data-ttu-id="e5fb4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fb4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fb4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fb4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5fb4-135">INPUTS</span></span>

### <span data-ttu-id="e5fb4-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e5fb4-136">BatchAccountContext</span></span>
<span data-ttu-id="e5fb4-137">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e5fb4-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="e5fb4-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="e5fb4-138">Byte[]</span></span>
<span data-ttu-id="e5fb4-139">O parâmetro ' RawData ' aceita o valor do tipo ' byte [] ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e5fb4-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="e5fb4-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5fb4-140">OUTPUTS</span></span>

## <span data-ttu-id="e5fb4-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5fb4-141">NOTES</span></span>

## <span data-ttu-id="e5fb4-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5fb4-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5fb4-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e5fb4-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="e5fb4-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e5fb4-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e5fb4-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e5fb4-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="e5fb4-146">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="e5fb4-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

