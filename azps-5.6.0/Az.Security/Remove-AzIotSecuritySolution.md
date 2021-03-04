---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: da98138060b0c06e09a56b375c64f530ea8e51f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889397"
---
# <span data-ttu-id="38bb3-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="38bb3-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="38bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="38bb3-103">Excluir solução de segurança de IoT</span><span class="sxs-lookup"><span data-stu-id="38bb3-103">Delete IoT security solution</span></span>

## <span data-ttu-id="38bb3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38bb3-104">SYNTAX</span></span>

### <span data-ttu-id="38bb3-105">ResourceGroupLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38bb3-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bb3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bb3-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38bb3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="38bb3-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bb3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38bb3-108">DESCRIPTION</span></span>
<span data-ttu-id="38bb3-109">O Remove-AzIotSecuritySolution cmdlet exclui uma solução de segurança iot específica.</span><span class="sxs-lookup"><span data-stu-id="38bb3-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="38bb3-110">A solução de segurança da IoT coleta dados e eventos de segurança de dispositivos iot e hub iot para ajudar a evitar e detectar ameaças.</span><span class="sxs-lookup"><span data-stu-id="38bb3-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="38bb3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="38bb3-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38bb3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="38bb3-113">Excluir solução de segurança da IoT "MySample" com o grupo de recursos "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="38bb3-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="38bb3-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38bb3-114">PARAMETERS</span></span>

### <span data-ttu-id="38bb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bb3-115">-DefaultProfile</span></span>
<span data-ttu-id="38bb3-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38bb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bb3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38bb3-117">-InputObject</span></span>
<span data-ttu-id="38bb3-118">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="38bb3-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="38bb3-119">-Name</span></span>
<span data-ttu-id="38bb3-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="38bb3-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38bb3-121">-PassThru</span></span>
<span data-ttu-id="38bb3-122">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="38bb3-122">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bb3-123">-ResourceGroupName</span></span>
<span data-ttu-id="38bb3-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38bb3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38bb3-125">-ResourceId</span></span>
<span data-ttu-id="38bb3-126">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="38bb3-126">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38bb3-127">-Confirm</span></span>
<span data-ttu-id="38bb3-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38bb3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bb3-129">-WhatIf</span></span>
<span data-ttu-id="38bb3-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38bb3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bb3-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38bb3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38bb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bb3-132">CommonParameters</span></span>
<span data-ttu-id="38bb3-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bb3-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bb3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bb3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38bb3-135">INPUTS</span></span>

### <span data-ttu-id="38bb3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="38bb3-136">System.String</span></span>

### <span data-ttu-id="38bb3-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="38bb3-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="38bb3-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38bb3-138">OUTPUTS</span></span>

### <span data-ttu-id="38bb3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38bb3-139">System.Boolean</span></span>

## <span data-ttu-id="38bb3-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="38bb3-140">NOTES</span></span>

## <span data-ttu-id="38bb3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38bb3-141">RELATED LINKS</span></span>
