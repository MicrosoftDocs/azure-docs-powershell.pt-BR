---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 099f6a1ea19e9810745715dbc90ea0e0b1962285
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890880"
---
# <span data-ttu-id="e3d55-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="e3d55-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="e3d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d55-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d55-103">Cancela uma exclusão com falha de um certificado.</span><span class="sxs-lookup"><span data-stu-id="e3d55-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="e3d55-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3d55-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3d55-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3d55-105">DESCRIPTION</span></span>
<span data-ttu-id="e3d55-106">O cmdlet **Stop-AzBatchCertificateDeletion** cancela uma exclusão com falha de um certificado no serviço batch do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d55-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="e3d55-107">Você só poderá interromper uma exclusão se o certificado estiver no estado **DeleteFailed.**</span><span class="sxs-lookup"><span data-stu-id="e3d55-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="e3d55-108">Este cmdlet restaura o certificado para o **estado** Ativo.</span><span class="sxs-lookup"><span data-stu-id="e3d55-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="e3d55-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3d55-109">EXAMPLES</span></span>

### <span data-ttu-id="e3d55-110">Exemplo 1: Cancelar uma exclusão</span><span class="sxs-lookup"><span data-stu-id="e3d55-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="e3d55-111">Esse comando cancela a exclusão do certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="e3d55-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="e3d55-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3d55-112">PARAMETERS</span></span>

### <span data-ttu-id="e3d55-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e3d55-113">-BatchContext</span></span>
<span data-ttu-id="e3d55-114">Especifica a instância **BatchAccountContext** que esse cmdlet usa para interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="e3d55-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e3d55-115">Se você usar o cmdlet Get-AzBatchAccount para obter seu BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço Batch.</span><span class="sxs-lookup"><span data-stu-id="e3d55-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e3d55-116">Para usar a autenticação de chave compartilhada, use o cmdlet Get-AzBatchAccountKey para obter um objeto BatchAccountContext com suas chaves de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="e3d55-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e3d55-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="e3d55-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e3d55-118">Para alterar a chave a ser usada, de definir a propriedade BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e3d55-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e3d55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d55-119">-DefaultProfile</span></span>
<span data-ttu-id="e3d55-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e3d55-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3d55-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="e3d55-121">-Thumbprint</span></span>
<span data-ttu-id="e3d55-122">Especifica a impressão digital do certificado que este cmdlet restaura para o **estado** Ativo.</span><span class="sxs-lookup"><span data-stu-id="e3d55-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="e3d55-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e3d55-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e3d55-124">Especifica o algoritmo usado para derivar o parâmetro *Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="e3d55-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e3d55-125">Atualmente, o único valor válido é sha1.</span><span class="sxs-lookup"><span data-stu-id="e3d55-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e3d55-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d55-126">CommonParameters</span></span>
<span data-ttu-id="e3d55-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d55-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d55-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3d55-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d55-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3d55-129">INPUTS</span></span>

### <span data-ttu-id="e3d55-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e3d55-130">System.String</span></span>

### <span data-ttu-id="e3d55-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e3d55-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e3d55-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3d55-132">OUTPUTS</span></span>

### <span data-ttu-id="e3d55-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="e3d55-133">System.Void</span></span>

## <span data-ttu-id="e3d55-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3d55-134">NOTES</span></span>

## <span data-ttu-id="e3d55-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3d55-135">RELATED LINKS</span></span>

[<span data-ttu-id="e3d55-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e3d55-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e3d55-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e3d55-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="e3d55-138">Cmdlets do Lote do Azure</span><span class="sxs-lookup"><span data-stu-id="e3d55-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
