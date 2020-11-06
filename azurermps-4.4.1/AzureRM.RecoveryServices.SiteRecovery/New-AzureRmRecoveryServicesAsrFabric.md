---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610468"
---
# <span data-ttu-id="06552-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06552-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="06552-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06552-102">SYNOPSIS</span></span>
<span data-ttu-id="06552-103">Cria uma malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="06552-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06552-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06552-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06552-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06552-105">DESCRIPTION</span></span>
<span data-ttu-id="06552-106">O cmdlet **New-AzureRmRecoveryServicesAsrFabric** cria uma malha de recuperação de site do Azure do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="06552-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="06552-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06552-107">EXAMPLES</span></span>

### <span data-ttu-id="06552-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06552-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="06552-109">Inicia a criação do Fabric com o nome passado e retorna o trabalho ASR usado para acompanhar a operação de criação do fabric.</span><span class="sxs-lookup"><span data-stu-id="06552-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="06552-110">OS</span><span class="sxs-lookup"><span data-stu-id="06552-110">PARAMETERS</span></span>

### <span data-ttu-id="06552-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="06552-111">-Name</span></span>
<span data-ttu-id="06552-112">Especifica o nome da malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="06552-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06552-113">-Digite</span><span class="sxs-lookup"><span data-stu-id="06552-113">-Type</span></span>
<span data-ttu-id="06552-114">Especifica o tipo de malha do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="06552-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06552-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06552-115">-Confirm</span></span>
<span data-ttu-id="06552-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06552-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06552-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06552-117">-WhatIf</span></span>
<span data-ttu-id="06552-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06552-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06552-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06552-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06552-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06552-120">CommonParameters</span></span>
<span data-ttu-id="06552-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06552-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06552-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06552-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06552-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06552-123">INPUTS</span></span>

### <span data-ttu-id="06552-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06552-124">None</span></span>

## <span data-ttu-id="06552-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06552-125">OUTPUTS</span></span>

### <span data-ttu-id="06552-126">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="06552-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="06552-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06552-127">NOTES</span></span>

## <span data-ttu-id="06552-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06552-128">RELATED LINKS</span></span>

[<span data-ttu-id="06552-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06552-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="06552-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06552-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
