---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 74178c9818cb5782c105e5566fd5e5dc44ef6526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440833"
---
# <span data-ttu-id="0b79e-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="0b79e-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="0b79e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b79e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b79e-103">Inicia a coleta de logs personalizados de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="0b79e-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b79e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b79e-104">SYNTAX</span></span>

### <span data-ttu-id="0b79e-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b79e-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b79e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0b79e-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b79e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b79e-107">DESCRIPTION</span></span>
<span data-ttu-id="0b79e-108">O cmdlet **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** inicia a coleta de logs personalizados de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0b79e-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="0b79e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b79e-109">EXAMPLES</span></span>

## <span data-ttu-id="0b79e-110">OS</span><span class="sxs-lookup"><span data-stu-id="0b79e-110">PARAMETERS</span></span>

### <span data-ttu-id="0b79e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b79e-111">-DefaultProfile</span></span>
<span data-ttu-id="0b79e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b79e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b79e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b79e-113">-ResourceGroupName</span></span>
<span data-ttu-id="0b79e-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="0b79e-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b79e-115">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="0b79e-115">-Workspace</span></span>
<span data-ttu-id="0b79e-116">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="0b79e-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b79e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0b79e-117">-WorkspaceName</span></span>
<span data-ttu-id="0b79e-118">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="0b79e-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b79e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b79e-119">-Confirm</span></span>
<span data-ttu-id="0b79e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b79e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b79e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b79e-121">-WhatIf</span></span>
<span data-ttu-id="0b79e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b79e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b79e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b79e-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b79e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b79e-124">CommonParameters</span></span>
<span data-ttu-id="0b79e-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b79e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b79e-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b79e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b79e-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b79e-127">INPUTS</span></span>

### <span data-ttu-id="0b79e-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0b79e-128">PSWorkspace</span></span>
<span data-ttu-id="0b79e-129">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0b79e-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0b79e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b79e-130">OUTPUTS</span></span>

### <span data-ttu-id="0b79e-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0b79e-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0b79e-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b79e-132">NOTES</span></span>
* <span data-ttu-id="0b79e-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="0b79e-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0b79e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b79e-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b79e-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="0b79e-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


