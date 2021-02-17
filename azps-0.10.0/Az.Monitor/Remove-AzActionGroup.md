---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 2e7240f607d2c9ed426c35f9427452640ceec84f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399338"
---
# <span data-ttu-id="84b37-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="84b37-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="84b37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84b37-102">SYNOPSIS</span></span>
<span data-ttu-id="84b37-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="84b37-103">Removes an action group.</span></span>

## <span data-ttu-id="84b37-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84b37-104">SYNTAX</span></span>

### <span data-ttu-id="84b37-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="84b37-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b37-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84b37-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84b37-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84b37-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b37-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="84b37-108">DESCRIPTION</span></span>
<span data-ttu-id="84b37-109">O **cmdlet Remove-AzActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="84b37-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="84b37-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84b37-110">EXAMPLES</span></span>

### <span data-ttu-id="84b37-111">Exemplo 1: Remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="84b37-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="84b37-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84b37-112">PARAMETERS</span></span>

### <span data-ttu-id="84b37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b37-113">-DefaultProfile</span></span>
<span data-ttu-id="84b37-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="84b37-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84b37-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84b37-115">-InputObject</span></span>
<span data-ttu-id="84b37-116">O recurso de grupo de ações</span><span class="sxs-lookup"><span data-stu-id="84b37-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b37-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="84b37-117">-Name</span></span>
<span data-ttu-id="84b37-118">O nome do grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="84b37-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b37-119">-ResourceGroupName</span></span>
<span data-ttu-id="84b37-120">A nam do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="84b37-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b37-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84b37-121">-ResourceId</span></span>
<span data-ttu-id="84b37-122">O recurso i</span><span class="sxs-lookup"><span data-stu-id="84b37-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b37-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="84b37-123">-Confirm</span></span>
<span data-ttu-id="84b37-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84b37-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b37-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b37-125">-WhatIf</span></span>
<span data-ttu-id="84b37-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="84b37-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84b37-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84b37-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b37-128">CommonParameters</span></span>
<span data-ttu-id="84b37-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b37-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84b37-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b37-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="84b37-131">INPUTS</span></span>

### <span data-ttu-id="84b37-132">System.String</span><span class="sxs-lookup"><span data-stu-id="84b37-132">System.String</span></span>

### <span data-ttu-id="84b37-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="84b37-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="84b37-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="84b37-134">OUTPUTS</span></span>

### <span data-ttu-id="84b37-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84b37-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="84b37-136">Notas</span><span class="sxs-lookup"><span data-stu-id="84b37-136">NOTES</span></span>

## <span data-ttu-id="84b37-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84b37-137">RELATED LINKS</span></span>

<span data-ttu-id="84b37-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="84b37-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

