---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112226"
---
# <span data-ttu-id="58368-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="58368-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="58368-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58368-102">SYNOPSIS</span></span>
<span data-ttu-id="58368-103">Cancela uma exclusão com falha de um certificado.</span><span class="sxs-lookup"><span data-stu-id="58368-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="58368-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58368-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58368-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="58368-105">DESCRIPTION</span></span>
<span data-ttu-id="58368-106">O cmdlet **Stop-AzBatchCertificateDeletion** cancela uma exclusão com falha de um certificado no serviço Lote do Azure.</span><span class="sxs-lookup"><span data-stu-id="58368-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="58368-107">Você só poderá interromper uma exclusão se o certificado estiver no estado **DeleteFailed.**</span><span class="sxs-lookup"><span data-stu-id="58368-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="58368-108">Este cmdlet restaura o certificado para o **estado** Ativo.</span><span class="sxs-lookup"><span data-stu-id="58368-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="58368-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58368-109">EXAMPLES</span></span>

### <span data-ttu-id="58368-110">Exemplo 1: Cancelar uma exclusão</span><span class="sxs-lookup"><span data-stu-id="58368-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="58368-111">Esse comando cancela a exclusão do certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="58368-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="58368-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58368-112">PARAMETERS</span></span>

### <span data-ttu-id="58368-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58368-113">-BatchContext</span></span>
<span data-ttu-id="58368-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="58368-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58368-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Lote.</span><span class="sxs-lookup"><span data-stu-id="58368-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="58368-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="58368-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="58368-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="58368-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="58368-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="58368-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="58368-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58368-119">-DefaultProfile</span></span>
<span data-ttu-id="58368-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="58368-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58368-121">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="58368-121">-Thumbprint</span></span>
<span data-ttu-id="58368-122">Especifica a impressão digital do certificado que este cmdlet restaura para o **estado** Ativo.</span><span class="sxs-lookup"><span data-stu-id="58368-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58368-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="58368-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="58368-124">Especifica o algoritmo usado para derivar o parâmetro *Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="58368-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="58368-125">Atualmente, o único valor válido é sha1.</span><span class="sxs-lookup"><span data-stu-id="58368-125">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58368-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58368-126">CommonParameters</span></span>
<span data-ttu-id="58368-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58368-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58368-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58368-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58368-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="58368-129">INPUTS</span></span>

### <span data-ttu-id="58368-130">System.String</span><span class="sxs-lookup"><span data-stu-id="58368-130">System.String</span></span>

### <span data-ttu-id="58368-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58368-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="58368-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="58368-132">OUTPUTS</span></span>

### <span data-ttu-id="58368-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="58368-133">System.Void</span></span>

## <span data-ttu-id="58368-134">Notas</span><span class="sxs-lookup"><span data-stu-id="58368-134">NOTES</span></span>

## <span data-ttu-id="58368-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58368-135">RELATED LINKS</span></span>

[<span data-ttu-id="58368-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="58368-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="58368-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="58368-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="58368-138">Cmdlets de lote do Azure</span><span class="sxs-lookup"><span data-stu-id="58368-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
