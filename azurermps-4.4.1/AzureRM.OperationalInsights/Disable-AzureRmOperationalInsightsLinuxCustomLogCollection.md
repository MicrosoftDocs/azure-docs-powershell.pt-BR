---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f222f075ec80162324d7ebcacfb4569371b59741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440600"
---
# <span data-ttu-id="cf162-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cf162-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="cf162-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf162-102">SYNOPSIS</span></span>
<span data-ttu-id="cf162-103">Interrompe a coleta de logs personalizados de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="cf162-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf162-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf162-104">SYNTAX</span></span>

### <span data-ttu-id="cf162-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf162-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf162-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cf162-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf162-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf162-107">DESCRIPTION</span></span>
<span data-ttu-id="cf162-108">O cmdlet **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** interrompe a coleta de logs personalizados de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf162-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cf162-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf162-109">EXAMPLES</span></span>

## <span data-ttu-id="cf162-110">OS</span><span class="sxs-lookup"><span data-stu-id="cf162-110">PARAMETERS</span></span>

### <span data-ttu-id="cf162-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf162-111">-ResourceGroupName</span></span>
<span data-ttu-id="cf162-112">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="cf162-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf162-113">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="cf162-113">-Workspace</span></span>
<span data-ttu-id="cf162-114">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="cf162-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf162-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf162-115">-WorkspaceName</span></span>
<span data-ttu-id="cf162-116">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="cf162-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf162-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cf162-117">-Confirm</span></span>
<span data-ttu-id="cf162-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf162-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf162-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf162-119">-WhatIf</span></span>
<span data-ttu-id="cf162-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf162-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf162-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf162-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf162-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf162-122">-DefaultProfile</span></span>
<span data-ttu-id="cf162-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf162-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf162-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf162-124">CommonParameters</span></span>
<span data-ttu-id="cf162-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf162-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf162-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf162-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf162-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf162-127">INPUTS</span></span>

### <span data-ttu-id="cf162-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf162-128">PSWorkspace</span></span>
<span data-ttu-id="cf162-129">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="cf162-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cf162-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf162-130">OUTPUTS</span></span>

### <span data-ttu-id="cf162-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cf162-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cf162-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf162-132">NOTES</span></span>
* <span data-ttu-id="cf162-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="cf162-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cf162-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf162-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf162-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cf162-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


