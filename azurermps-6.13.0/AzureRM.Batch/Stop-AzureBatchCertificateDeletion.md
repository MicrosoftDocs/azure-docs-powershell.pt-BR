---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431399"
---
# <span data-ttu-id="6fb9e-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="6fb9e-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="6fb9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb9e-103">Cancela uma falha na exclusão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fb9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fb9e-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fb9e-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb9e-106">O cmdlet **Stop-AzureBatchCertificateDeletion** cancela uma falha na exclusão de um certificado no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="6fb9e-107">Você pode parar uma exclusão apenas se o certificado estiver no estado **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="6fb9e-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="6fb9e-108">Isso cmldet restaura o certificado ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="6fb9e-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="6fb9e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fb9e-109">EXAMPLES</span></span>

### <span data-ttu-id="6fb9e-110">Exemplo 1: cancelar uma exclusão</span><span class="sxs-lookup"><span data-stu-id="6fb9e-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="6fb9e-111">Esse comando cancela a exclusão do certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="6fb9e-112">OS</span><span class="sxs-lookup"><span data-stu-id="6fb9e-112">PARAMETERS</span></span>

### <span data-ttu-id="6fb9e-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6fb9e-113">-BatchContext</span></span>
<span data-ttu-id="6fb9e-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6fb9e-115">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6fb9e-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6fb9e-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6fb9e-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6fb9e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb9e-119">-DefaultProfile</span></span>
<span data-ttu-id="6fb9e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb9e-121">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="6fb9e-121">-Thumbprint</span></span>
<span data-ttu-id="6fb9e-122">Especifica a impressão digital do certificado que este cmdlet restaura ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="6fb9e-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="6fb9e-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6fb9e-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6fb9e-124">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="6fb9e-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="6fb9e-125">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="6fb9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb9e-126">CommonParameters</span></span>
<span data-ttu-id="6fb9e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb9e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb9e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fb9e-129">INPUTS</span></span>

### <span data-ttu-id="6fb9e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fb9e-130">System.String</span></span>

### <span data-ttu-id="6fb9e-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6fb9e-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="6fb9e-132">Parâmetros: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fb9e-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="6fb9e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fb9e-133">OUTPUTS</span></span>

### <span data-ttu-id="6fb9e-134">System. void</span><span class="sxs-lookup"><span data-stu-id="6fb9e-134">System.Void</span></span>

## <span data-ttu-id="6fb9e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fb9e-135">NOTES</span></span>

## <span data-ttu-id="6fb9e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fb9e-136">RELATED LINKS</span></span>

[<span data-ttu-id="6fb9e-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6fb9e-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6fb9e-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="6fb9e-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="6fb9e-139">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="6fb9e-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


