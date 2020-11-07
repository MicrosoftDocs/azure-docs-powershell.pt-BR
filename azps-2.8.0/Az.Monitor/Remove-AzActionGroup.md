---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: c026d161c0d5a3ac73d2736d19422ce45b59fbd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772168"
---
# <span data-ttu-id="10546-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="10546-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="10546-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10546-102">SYNOPSIS</span></span>
<span data-ttu-id="10546-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="10546-103">Removes an action group.</span></span>

## <span data-ttu-id="10546-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10546-104">SYNTAX</span></span>

### <span data-ttu-id="10546-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="10546-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10546-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10546-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10546-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10546-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10546-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10546-108">DESCRIPTION</span></span>
<span data-ttu-id="10546-109">O cmdlet **Remove-AzActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="10546-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="10546-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10546-110">EXAMPLES</span></span>

### <span data-ttu-id="10546-111">Exemplo 1: remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="10546-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="10546-112">OS</span><span class="sxs-lookup"><span data-stu-id="10546-112">PARAMETERS</span></span>

### <span data-ttu-id="10546-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10546-113">-DefaultProfile</span></span>
<span data-ttu-id="10546-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="10546-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10546-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10546-115">-InputObject</span></span>
<span data-ttu-id="10546-116">O recurso grupo de ações</span><span class="sxs-lookup"><span data-stu-id="10546-116">The action group resource</span></span>

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

### <span data-ttu-id="10546-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="10546-117">-Name</span></span>
<span data-ttu-id="10546-118">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="10546-118">The name of the action group.</span></span>

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

### <span data-ttu-id="10546-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10546-119">-ResourceGroupName</span></span>
<span data-ttu-id="10546-120">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="10546-120">The resource group nam</span></span>

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

### <span data-ttu-id="10546-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10546-121">-ResourceId</span></span>
<span data-ttu-id="10546-122">O recurso i</span><span class="sxs-lookup"><span data-stu-id="10546-122">The resource i</span></span>

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

### <span data-ttu-id="10546-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10546-123">-Confirm</span></span>
<span data-ttu-id="10546-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10546-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10546-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10546-125">-WhatIf</span></span>
<span data-ttu-id="10546-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10546-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10546-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10546-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10546-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10546-128">CommonParameters</span></span>
<span data-ttu-id="10546-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10546-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10546-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10546-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10546-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10546-131">INPUTS</span></span>

### <span data-ttu-id="10546-132">System. String</span><span class="sxs-lookup"><span data-stu-id="10546-132">System.String</span></span>

### <span data-ttu-id="10546-133">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="10546-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="10546-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10546-134">OUTPUTS</span></span>

### <span data-ttu-id="10546-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="10546-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="10546-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10546-136">NOTES</span></span>

## <span data-ttu-id="10546-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10546-137">RELATED LINKS</span></span>

<span data-ttu-id="10546-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="10546-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>