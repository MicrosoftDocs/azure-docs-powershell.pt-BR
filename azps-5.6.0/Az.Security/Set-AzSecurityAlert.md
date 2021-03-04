---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 889e4a0651c9aa3ccbe91227db803958fcb3c7bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889747"
---
# <span data-ttu-id="529f2-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="529f2-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="529f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="529f2-102">SYNOPSIS</span></span>
<span data-ttu-id="529f2-103">Atualiza um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="529f2-103">Updates a security alert state.</span></span>

## <span data-ttu-id="529f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="529f2-104">SYNTAX</span></span>

### <span data-ttu-id="529f2-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="529f2-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529f2-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="529f2-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="529f2-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="529f2-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="529f2-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529f2-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="529f2-109">DESCRIPTION</span></span>
<span data-ttu-id="529f2-110">Define um estado de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="529f2-110">Sets a security alert state.</span></span>

## <span data-ttu-id="529f2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="529f2-111">EXAMPLES</span></span>

### <span data-ttu-id="529f2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="529f2-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="529f2-113">Descarta um alerta de segurança que foi gerado.</span><span class="sxs-lookup"><span data-stu-id="529f2-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="529f2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="529f2-114">PARAMETERS</span></span>

### <span data-ttu-id="529f2-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="529f2-115">-ActionType</span></span>
<span data-ttu-id="529f2-116">Tipo de ação.</span><span class="sxs-lookup"><span data-stu-id="529f2-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529f2-117">-DefaultProfile</span></span>
<span data-ttu-id="529f2-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="529f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="529f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="529f2-119">-InputObject</span></span>
<span data-ttu-id="529f2-120">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="529f2-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-121">-Location</span><span class="sxs-lookup"><span data-stu-id="529f2-121">-Location</span></span>
<span data-ttu-id="529f2-122">Local.</span><span class="sxs-lookup"><span data-stu-id="529f2-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="529f2-123">-Name</span></span>
<span data-ttu-id="529f2-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="529f2-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="529f2-125">-PassThru</span></span>
<span data-ttu-id="529f2-126">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="529f2-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="529f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="529f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="529f2-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="529f2-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="529f2-129">-ResourceId</span></span>
<span data-ttu-id="529f2-130">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="529f2-130">Resource ID.</span></span>

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

### <span data-ttu-id="529f2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="529f2-131">-Confirm</span></span>
<span data-ttu-id="529f2-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="529f2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="529f2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529f2-133">-WhatIf</span></span>
<span data-ttu-id="529f2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="529f2-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="529f2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="529f2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="529f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529f2-136">CommonParameters</span></span>
<span data-ttu-id="529f2-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529f2-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="529f2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529f2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="529f2-139">INPUTS</span></span>

### <span data-ttu-id="529f2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="529f2-140">System.String</span></span>

### <span data-ttu-id="529f2-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="529f2-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="529f2-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="529f2-142">OUTPUTS</span></span>

### <span data-ttu-id="529f2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="529f2-143">System.Boolean</span></span>

## <span data-ttu-id="529f2-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="529f2-144">NOTES</span></span>

## <span data-ttu-id="529f2-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="529f2-145">RELATED LINKS</span></span>
