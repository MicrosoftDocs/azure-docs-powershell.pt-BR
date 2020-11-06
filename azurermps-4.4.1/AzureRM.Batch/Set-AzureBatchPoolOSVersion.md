---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603406"
---
# <span data-ttu-id="263fa-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="263fa-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="263fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="263fa-102">SYNOPSIS</span></span>
<span data-ttu-id="263fa-103">Altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="263fa-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="263fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="263fa-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="263fa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="263fa-105">DESCRIPTION</span></span>
<span data-ttu-id="263fa-106">O cmdlet **set-AzureBatchPoolOSVersion** altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="263fa-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="263fa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="263fa-107">EXAMPLES</span></span>

### <span data-ttu-id="263fa-108">Exemplo 1: definir a versão do sistema operacional de destino de um pool</span><span class="sxs-lookup"><span data-stu-id="263fa-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="263fa-109">Esse comando define a versão do sistema operacional de destino do pool mypool como WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="263fa-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="263fa-110">OS</span><span class="sxs-lookup"><span data-stu-id="263fa-110">PARAMETERS</span></span>

### <span data-ttu-id="263fa-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="263fa-111">-BatchContext</span></span>
<span data-ttu-id="263fa-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="263fa-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="263fa-113">Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="263fa-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="263fa-114">-ID</span><span class="sxs-lookup"><span data-stu-id="263fa-114">-Id</span></span>
<span data-ttu-id="263fa-115">Especifica a ID do pool.</span><span class="sxs-lookup"><span data-stu-id="263fa-115">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263fa-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="263fa-116">-TargetOSVersion</span></span>
<span data-ttu-id="263fa-117">Especifica a versão do sistema operacional do Azure Guest a ser instalada nas máquinas virtuais do pool.</span><span class="sxs-lookup"><span data-stu-id="263fa-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="263fa-118">Para obter mais informações sobre as versões do sistema operacional convidado do Azure, consulte versões do sistema operacional do Azure Guest e matriz de compatibilidade do SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="263fa-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263fa-119">-DefaultProfile</span></span>
<span data-ttu-id="263fa-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="263fa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="263fa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263fa-121">CommonParameters</span></span>
<span data-ttu-id="263fa-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263fa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263fa-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="263fa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263fa-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="263fa-124">INPUTS</span></span>

### <span data-ttu-id="263fa-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="263fa-125">BatchAccountContext</span></span>
<span data-ttu-id="263fa-126">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="263fa-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="263fa-127">String</span><span class="sxs-lookup"><span data-stu-id="263fa-127">String</span></span>
<span data-ttu-id="263fa-128">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="263fa-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="263fa-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="263fa-129">OUTPUTS</span></span>

## <span data-ttu-id="263fa-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="263fa-130">NOTES</span></span>

## <span data-ttu-id="263fa-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="263fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="263fa-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="263fa-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


