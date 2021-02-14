---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115982"
---
# <span data-ttu-id="d3e1e-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d3e1e-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="d3e1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e1e-103">Adiciona um certificado à conta em lote especificada.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="d3e1e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3e1e-104">SYNTAX</span></span>

### <span data-ttu-id="d3e1e-105">Arquivo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d3e1e-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3e1e-106">Rawdata</span><span class="sxs-lookup"><span data-stu-id="d3e1e-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3e1e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="d3e1e-108">O **cmdlet New-AzBatchCertificate** adiciona um certificado à conta especificada do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d3e1e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3e1e-109">EXAMPLES</span></span>

### <span data-ttu-id="d3e1e-110">Exemplo 1: Adicionar um certificado de um arquivo</span><span class="sxs-lookup"><span data-stu-id="d3e1e-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="d3e1e-111">Esse comando adiciona um certificado à conta em lote especificada usando o arquivo E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="d3e1e-112">Exemplo 2: Adicionar um certificado de dados brutos</span><span class="sxs-lookup"><span data-stu-id="d3e1e-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="d3e1e-113">O primeiro comando lê os dados do arquivo chamado MyCert.pfx para a variável $RawData dados.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="d3e1e-114">O segundo comando adiciona um certificado à conta Em lotes especificada usando os dados brutos armazenados em $RawData.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="d3e1e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3e1e-115">PARAMETERS</span></span>

### <span data-ttu-id="d3e1e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3e1e-116">-BatchContext</span></span>
<span data-ttu-id="d3e1e-117">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3e1e-118">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d3e1e-119">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d3e1e-120">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d3e1e-121">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d3e1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e1e-122">-DefaultProfile</span></span>
<span data-ttu-id="d3e1e-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3e1e-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d3e1e-124">-FilePath</span></span>
<span data-ttu-id="d3e1e-125">Especifica o caminho do arquivo de certificado.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="d3e1e-126">O arquivo de certificado deve estar no formato .cer ou .pfx.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d3e1e-127">-Tipo</span><span class="sxs-lookup"><span data-stu-id="d3e1e-127">-Kind</span></span>
<span data-ttu-id="d3e1e-128">O tipo de certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-128">The kind of certificate to create.</span></span> <span data-ttu-id="d3e1e-129">Se isso não for especificado, será presumido que todos os certificados sem senha sejam CER e todos os certificados com senha sejam PFX.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e1e-130">-Senha</span><span class="sxs-lookup"><span data-stu-id="d3e1e-130">-Password</span></span>
<span data-ttu-id="d3e1e-131">Especifica a senha para acessar a chave privada do certificado.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="d3e1e-132">Você deve especificar esse parâmetro se especificar um certificado no formato .pfx.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="d3e1e-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="d3e1e-133">-RawData</span></span>
<span data-ttu-id="d3e1e-134">Especifica os dados de certificado bruto no formato .cer ou .pfx.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d3e1e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e1e-135">CommonParameters</span></span>
<span data-ttu-id="d3e1e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e1e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e1e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3e1e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e1e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="d3e1e-138">INPUTS</span></span>

### <span data-ttu-id="d3e1e-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="d3e1e-139">System.Byte[]</span></span>

### <span data-ttu-id="d3e1e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3e1e-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d3e1e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="d3e1e-141">OUTPUTS</span></span>

### <span data-ttu-id="d3e1e-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="d3e1e-142">System.Void</span></span>

## <span data-ttu-id="d3e1e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="d3e1e-143">NOTES</span></span>

## <span data-ttu-id="d3e1e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3e1e-144">RELATED LINKS</span></span>

[<span data-ttu-id="d3e1e-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d3e1e-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="d3e1e-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d3e1e-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d3e1e-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d3e1e-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d3e1e-148">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="d3e1e-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
