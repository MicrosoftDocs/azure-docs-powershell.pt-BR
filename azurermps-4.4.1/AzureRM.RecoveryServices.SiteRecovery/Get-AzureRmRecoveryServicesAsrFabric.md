---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427815"
---
# <span data-ttu-id="dd1de-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="dd1de-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="dd1de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd1de-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1de-103">Obtenha os detalhes de uma malha de recuperação do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1de-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd1de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd1de-104">SYNTAX</span></span>

### <span data-ttu-id="dd1de-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd1de-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="dd1de-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dd1de-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="dd1de-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd1de-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="dd1de-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd1de-108">DESCRIPTION</span></span>
<span data-ttu-id="dd1de-109">O cmdlet **Get-AzureRmRecoveryServicesAsrFabric** Obtém as propriedades de uma malha de recuperação de site do Azure especificada ou todas as malhas do Azure site Recovery em um cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dd1de-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="dd1de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd1de-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1de-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd1de-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="dd1de-112">Retorna todas as malhas do Azure site Recovery no cofre.</span><span class="sxs-lookup"><span data-stu-id="dd1de-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="dd1de-113">OS</span><span class="sxs-lookup"><span data-stu-id="dd1de-113">PARAMETERS</span></span>

### <span data-ttu-id="dd1de-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd1de-114">-FriendlyName</span></span>
<span data-ttu-id="dd1de-115">Procure a malha ASR pelo nome amigável da malha.</span><span class="sxs-lookup"><span data-stu-id="dd1de-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1de-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd1de-116">-Name</span></span>
<span data-ttu-id="dd1de-117">Procure a malha ASR pelo nome da malha.</span><span class="sxs-lookup"><span data-stu-id="dd1de-117">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1de-118">CommonParameters</span></span>
<span data-ttu-id="dd1de-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1de-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1de-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1de-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd1de-121">INPUTS</span></span>

### <span data-ttu-id="dd1de-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dd1de-122">None</span></span>

## <span data-ttu-id="dd1de-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd1de-123">OUTPUTS</span></span>

### <span data-ttu-id="dd1de-124">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. Recoveryservices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dd1de-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dd1de-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd1de-125">NOTES</span></span>

## <span data-ttu-id="dd1de-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd1de-126">RELATED LINKS</span></span>

[<span data-ttu-id="dd1de-127">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="dd1de-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="dd1de-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="dd1de-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
