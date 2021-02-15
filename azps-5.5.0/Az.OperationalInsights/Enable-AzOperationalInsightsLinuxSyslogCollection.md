---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114074"
---
# <span data-ttu-id="6c32a-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6c32a-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="6c32a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c32a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c32a-103">Inicia a coleta de dados de syslog de computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="6c32a-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="6c32a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c32a-104">SYNTAX</span></span>

### <span data-ttu-id="6c32a-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6c32a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c32a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6c32a-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c32a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c32a-107">DESCRIPTION</span></span>
<span data-ttu-id="6c32a-108">O cmdlet **Enable-AzOperationalInsightsLinuxSyslogCollection** inicia o conjunto de dados de syslog de computadores Linux conectados em um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6c32a-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="6c32a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c32a-109">EXAMPLES</span></span>

## <span data-ttu-id="6c32a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c32a-110">PARAMETERS</span></span>

### <span data-ttu-id="6c32a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c32a-111">-DefaultProfile</span></span>
<span data-ttu-id="6c32a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6c32a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c32a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c32a-113">-ResourceGroupName</span></span>
<span data-ttu-id="6c32a-114">Especifica o nome de um grupo de recursos que contém computadores Linux.</span><span class="sxs-lookup"><span data-stu-id="6c32a-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6c32a-115">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="6c32a-115">-Workspace</span></span>
<span data-ttu-id="6c32a-116">Especifica um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="6c32a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c32a-117">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="6c32a-117">-WorkspaceName</span></span>
<span data-ttu-id="6c32a-118">Especifica o nome de um espaço de trabalho no qual este cmdlet opera.</span><span class="sxs-lookup"><span data-stu-id="6c32a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6c32a-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6c32a-119">-Confirm</span></span>
<span data-ttu-id="6c32a-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c32a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c32a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c32a-121">-WhatIf</span></span>
<span data-ttu-id="6c32a-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6c32a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c32a-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c32a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c32a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c32a-124">CommonParameters</span></span>
<span data-ttu-id="6c32a-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c32a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c32a-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c32a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c32a-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="6c32a-127">INPUTS</span></span>

### <span data-ttu-id="6c32a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c32a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6c32a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6c32a-129">System.String</span></span>

## <span data-ttu-id="6c32a-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="6c32a-130">OUTPUTS</span></span>

### <span data-ttu-id="6c32a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6c32a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6c32a-132">Notas</span><span class="sxs-lookup"><span data-stu-id="6c32a-132">NOTES</span></span>
* <span data-ttu-id="6c32a-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="6c32a-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6c32a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c32a-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c32a-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6c32a-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="6c32a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="6c32a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


