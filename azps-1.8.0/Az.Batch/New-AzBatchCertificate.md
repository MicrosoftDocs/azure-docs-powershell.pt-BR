---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: d0fefe06ad5392d2fe50552203a08872eea4e61f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93601859"
---
# <span data-ttu-id="439a6-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="439a6-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="439a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="439a6-102">SYNOPSIS</span></span>
<span data-ttu-id="439a6-103">Adiciona um certificado à conta em lotes especificada.</span><span class="sxs-lookup"><span data-stu-id="439a6-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="439a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="439a6-104">SYNTAX</span></span>

### <span data-ttu-id="439a6-105">Arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="439a6-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="439a6-106">RawData</span><span class="sxs-lookup"><span data-stu-id="439a6-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="439a6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="439a6-107">DESCRIPTION</span></span>
<span data-ttu-id="439a6-108">O cmdlet **New-AzBatchCertificate** adiciona um certificado à conta em lotes do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="439a6-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="439a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="439a6-109">EXAMPLES</span></span>

### <span data-ttu-id="439a6-110">Exemplo 1: adicionar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="439a6-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="439a6-111">Esse comando adiciona um certificado à conta em lotes especificada usando o arquivo E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="439a6-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="439a6-112">Exemplo 2: adicionar um certificado de dados brutos</span><span class="sxs-lookup"><span data-stu-id="439a6-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="439a6-113">O primeiro comando lê os dados do arquivo chamado MyCert. pfx na variável $RawData.</span><span class="sxs-lookup"><span data-stu-id="439a6-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="439a6-114">O segundo comando adiciona um certificado à conta em lotes especificada usando os dados brutos armazenados em $RawData.</span><span class="sxs-lookup"><span data-stu-id="439a6-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="439a6-115">OS</span><span class="sxs-lookup"><span data-stu-id="439a6-115">PARAMETERS</span></span>

### <span data-ttu-id="439a6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="439a6-116">-BatchContext</span></span>
<span data-ttu-id="439a6-117">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="439a6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="439a6-118">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="439a6-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="439a6-119">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="439a6-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="439a6-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="439a6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="439a6-121">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="439a6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="439a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439a6-122">-DefaultProfile</span></span>
<span data-ttu-id="439a6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="439a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="439a6-124">-FilePath</span></span>
<span data-ttu-id="439a6-125">Especifica o caminho do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="439a6-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="439a6-126">O arquivo de certificado deve estar em um formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="439a6-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="439a6-127">-Senha</span><span class="sxs-lookup"><span data-stu-id="439a6-127">-Password</span></span>
<span data-ttu-id="439a6-128">Especifica a senha para acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="439a6-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="439a6-129">Você deve especificar esse parâmetro se especificar um certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="439a6-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439a6-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="439a6-130">-RawData</span></span>
<span data-ttu-id="439a6-131">Especifica os dados brutos do certificado em formato. cer ou. pfx.</span><span class="sxs-lookup"><span data-stu-id="439a6-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="439a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439a6-132">CommonParameters</span></span>
<span data-ttu-id="439a6-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439a6-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439a6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="439a6-135">INPUTS</span></span>

### <span data-ttu-id="439a6-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="439a6-136">System.Byte[]</span></span>

### <span data-ttu-id="439a6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="439a6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="439a6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="439a6-138">OUTPUTS</span></span>

### <span data-ttu-id="439a6-139">System. void</span><span class="sxs-lookup"><span data-stu-id="439a6-139">System.Void</span></span>

## <span data-ttu-id="439a6-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="439a6-140">NOTES</span></span>

## <span data-ttu-id="439a6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="439a6-141">RELATED LINKS</span></span>

[<span data-ttu-id="439a6-142">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="439a6-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="439a6-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="439a6-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="439a6-144">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="439a6-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="439a6-145">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="439a6-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


