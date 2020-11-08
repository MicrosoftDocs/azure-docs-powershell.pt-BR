---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125858"
---
# <span data-ttu-id="1e821-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1e821-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="1e821-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e821-102">SYNOPSIS</span></span>
<span data-ttu-id="1e821-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="1e821-103">Removes an action group.</span></span>

## <span data-ttu-id="1e821-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e821-104">SYNTAX</span></span>

### <span data-ttu-id="1e821-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e821-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e821-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e821-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e821-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e821-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e821-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e821-108">DESCRIPTION</span></span>
<span data-ttu-id="1e821-109">O cmdlet **Remove-AzActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="1e821-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="1e821-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e821-110">EXAMPLES</span></span>

### <span data-ttu-id="1e821-111">Exemplo 1: remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="1e821-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="1e821-112">OS</span><span class="sxs-lookup"><span data-stu-id="1e821-112">PARAMETERS</span></span>

### <span data-ttu-id="1e821-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e821-113">-DefaultProfile</span></span>
<span data-ttu-id="1e821-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1e821-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e821-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e821-115">-InputObject</span></span>
<span data-ttu-id="1e821-116">O recurso grupo de ações</span><span class="sxs-lookup"><span data-stu-id="1e821-116">The action group resource</span></span>

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

### <span data-ttu-id="1e821-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e821-117">-Name</span></span>
<span data-ttu-id="1e821-118">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="1e821-118">The name of the action group.</span></span>

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

### <span data-ttu-id="1e821-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e821-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e821-120">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1e821-120">The resource group nam</span></span>

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

### <span data-ttu-id="1e821-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e821-121">-ResourceId</span></span>
<span data-ttu-id="1e821-122">O recurso i</span><span class="sxs-lookup"><span data-stu-id="1e821-122">The resource i</span></span>

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

### <span data-ttu-id="1e821-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e821-123">-Confirm</span></span>
<span data-ttu-id="1e821-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e821-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e821-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e821-125">-WhatIf</span></span>
<span data-ttu-id="1e821-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e821-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e821-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e821-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e821-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e821-128">CommonParameters</span></span>
<span data-ttu-id="1e821-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e821-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e821-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e821-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e821-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e821-131">INPUTS</span></span>

### <span data-ttu-id="1e821-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e821-132">System.String</span></span>

### <span data-ttu-id="1e821-133">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1e821-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1e821-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e821-134">OUTPUTS</span></span>

### <span data-ttu-id="1e821-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1e821-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1e821-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e821-136">NOTES</span></span>

## <span data-ttu-id="1e821-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e821-137">RELATED LINKS</span></span>

<span data-ttu-id="1e821-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1e821-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
