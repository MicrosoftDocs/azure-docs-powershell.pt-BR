---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: e429a17d65a2c35f6961b3d68de4267ca91c4658
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609618"
---
# <span data-ttu-id="bcf4c-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="bcf4c-101">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="bcf4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf4c-103">Inicia a coleta de dados do syslog a partir de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-103">Starts collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcf4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcf4c-104">SYNTAX</span></span>

### <span data-ttu-id="bcf4c-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bcf4c-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf4c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bcf4c-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf4c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcf4c-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf4c-108">O cmdlet **Enable-AzureRmOperationalInsightsLinuxSyslogCollection** inicia a coleta de dados de syslog de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-108">The **Enable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bcf4c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcf4c-109">EXAMPLES</span></span>

## <span data-ttu-id="bcf4c-110">OS</span><span class="sxs-lookup"><span data-stu-id="bcf4c-110">PARAMETERS</span></span>

### <span data-ttu-id="bcf4c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf4c-111">-ResourceGroupName</span></span>
<span data-ttu-id="bcf4c-112">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-112">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="bcf4c-113">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bcf4c-113">-Workspace</span></span>
<span data-ttu-id="bcf4c-114">Especifica um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bcf4c-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcf4c-115">-WorkspaceName</span></span>
<span data-ttu-id="bcf4c-116">Especifica o nome de um espaço de trabalho no qual esse cmdlet Opera.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bcf4c-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcf4c-117">-Confirm</span></span>
<span data-ttu-id="bcf4c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf4c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf4c-119">-WhatIf</span></span>
<span data-ttu-id="bcf4c-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf4c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf4c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf4c-122">-DefaultProfile</span></span>
<span data-ttu-id="bcf4c-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf4c-124">CommonParameters</span></span>
<span data-ttu-id="bcf4c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf4c-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf4c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf4c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcf4c-127">INPUTS</span></span>

### <span data-ttu-id="bcf4c-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bcf4c-128">PSWorkspace</span></span>
<span data-ttu-id="bcf4c-129">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bcf4c-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bcf4c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcf4c-130">OUTPUTS</span></span>

### <span data-ttu-id="bcf4c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bcf4c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bcf4c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcf4c-132">NOTES</span></span>
* <span data-ttu-id="bcf4c-133">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, insights</span><span class="sxs-lookup"><span data-stu-id="bcf4c-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bcf4c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcf4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="bcf4c-135">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="bcf4c-135">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="bcf4c-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="bcf4c-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


