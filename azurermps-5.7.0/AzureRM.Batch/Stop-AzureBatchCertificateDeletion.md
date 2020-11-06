---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 51fca07847ca5bf0c73a5f2c88a41d3de166053c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427676"
---
# <span data-ttu-id="c69a8-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="c69a8-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="c69a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c69a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c69a8-103">Cancela uma falha na exclusão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="c69a8-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c69a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c69a8-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c69a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c69a8-106">O cmdlet **Stop-AzureBatchCertificateDeletion** cancela uma falha na exclusão de um certificado no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a8-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="c69a8-107">Você pode parar uma exclusão apenas se o certificado estiver no estado **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="c69a8-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="c69a8-108">Isso cmldet restaura o certificado ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="c69a8-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="c69a8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c69a8-109">EXAMPLES</span></span>

### <span data-ttu-id="c69a8-110">Exemplo 1: cancelar uma exclusão</span><span class="sxs-lookup"><span data-stu-id="c69a8-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="c69a8-111">Esse comando cancela a exclusão do certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="c69a8-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="c69a8-112">OS</span><span class="sxs-lookup"><span data-stu-id="c69a8-112">PARAMETERS</span></span>

### <span data-ttu-id="c69a8-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c69a8-113">-BatchContext</span></span>
<span data-ttu-id="c69a8-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c69a8-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c69a8-115">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="c69a8-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c69a8-116">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="c69a8-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c69a8-117">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c69a8-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c69a8-118">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c69a8-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c69a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69a8-119">-DefaultProfile</span></span>
<span data-ttu-id="c69a8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c69a8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c69a8-121">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="c69a8-121">-Thumbprint</span></span>
<span data-ttu-id="c69a8-122">Especifica a impressão digital do certificado que este cmdlet restaura ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="c69a8-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69a8-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c69a8-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c69a8-124">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="c69a8-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="c69a8-125">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="c69a8-125">Currently, the only valid value is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69a8-126">CommonParameters</span></span>
<span data-ttu-id="c69a8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69a8-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69a8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69a8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c69a8-129">INPUTS</span></span>

### <span data-ttu-id="c69a8-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c69a8-130">BatchAccountContext</span></span>
<span data-ttu-id="c69a8-131">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="c69a8-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c69a8-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c69a8-132">OUTPUTS</span></span>

## <span data-ttu-id="c69a8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c69a8-133">NOTES</span></span>

## <span data-ttu-id="c69a8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c69a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="c69a8-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c69a8-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c69a8-136">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c69a8-136">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="c69a8-137">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="c69a8-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


