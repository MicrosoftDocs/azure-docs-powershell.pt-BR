---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431799"
---
# <span data-ttu-id="ace38-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="ace38-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="ace38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ace38-102">SYNOPSIS</span></span>
<span data-ttu-id="ace38-103">Cancela uma falha na exclusão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="ace38-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ace38-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ace38-105">DESCRIPTION</span></span>
<span data-ttu-id="ace38-106">O cmdlet **Stop-AzureBatchCertificateDeletion** cancela uma falha na exclusão de um certificado no serviço em lotes do Azure.</span><span class="sxs-lookup"><span data-stu-id="ace38-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="ace38-107">Você pode parar uma exclusão apenas se o certificado estiver no estado **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="ace38-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="ace38-108">Isso cmldet restaura o certificado ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="ace38-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="ace38-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ace38-109">EXAMPLES</span></span>

### <span data-ttu-id="ace38-110">Exemplo 1: cancelar uma exclusão</span><span class="sxs-lookup"><span data-stu-id="ace38-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="ace38-111">Esse comando cancela a exclusão do certificado que tem a impressão digital especificada.</span><span class="sxs-lookup"><span data-stu-id="ace38-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="ace38-112">OS</span><span class="sxs-lookup"><span data-stu-id="ace38-112">PARAMETERS</span></span>

### <span data-ttu-id="ace38-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ace38-113">-BatchContext</span></span>
<span data-ttu-id="ace38-114">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="ace38-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ace38-115">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ace38-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ace38-116">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="ace38-116">-Thumbprint</span></span>
<span data-ttu-id="ace38-117">Especifica a impressão digital do certificado que este cmdlet restaura ao estado **ativo** .</span><span class="sxs-lookup"><span data-stu-id="ace38-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="ace38-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ace38-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ace38-119">Especifica o algoritmo usado para derivar o parâmetro de *impressão digital* .</span><span class="sxs-lookup"><span data-stu-id="ace38-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ace38-120">No momento, o único valor válido é SHA1.</span><span class="sxs-lookup"><span data-stu-id="ace38-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="ace38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace38-121">-DefaultProfile</span></span>
<span data-ttu-id="ace38-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ace38-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ace38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace38-123">CommonParameters</span></span>
<span data-ttu-id="ace38-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace38-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace38-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace38-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ace38-126">INPUTS</span></span>

### <span data-ttu-id="ace38-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ace38-127">BatchAccountContext</span></span>
<span data-ttu-id="ace38-128">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ace38-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ace38-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ace38-129">OUTPUTS</span></span>

## <span data-ttu-id="ace38-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ace38-130">NOTES</span></span>

## <span data-ttu-id="ace38-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ace38-131">RELATED LINKS</span></span>

[<span data-ttu-id="ace38-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ace38-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ace38-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ace38-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="ace38-134">Cmdlets do Azure batch</span><span class="sxs-lookup"><span data-stu-id="ace38-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


