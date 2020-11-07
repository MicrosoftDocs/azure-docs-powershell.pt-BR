---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785766"
---
# <span data-ttu-id="e4f6b-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e4f6b-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="e4f6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f6b-103">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4f6b-104">SYNTAX</span></span>

### <span data-ttu-id="e4f6b-105">ByPropertyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4f6b-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4f6b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f6b-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4f6b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4f6b-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f6b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4f6b-108">DESCRIPTION</span></span>
<span data-ttu-id="e4f6b-109">O cmdlet **Remove-AzureRmActionGroup** remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="e4f6b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4f6b-110">EXAMPLES</span></span>

### <span data-ttu-id="e4f6b-111">Exemplo 1: remover um grupo de ações</span><span class="sxs-lookup"><span data-stu-id="e4f6b-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="e4f6b-112">OS</span><span class="sxs-lookup"><span data-stu-id="e4f6b-112">PARAMETERS</span></span>

### <span data-ttu-id="e4f6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f6b-113">-DefaultProfile</span></span>
<span data-ttu-id="e4f6b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e4f6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4f6b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4f6b-115">-InputObject</span></span>
<span data-ttu-id="e4f6b-116">O grupo de ação resourc</span><span class="sxs-lookup"><span data-stu-id="e4f6b-116">The action group resourc</span></span>

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

### <span data-ttu-id="e4f6b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4f6b-117">-Name</span></span>
<span data-ttu-id="e4f6b-118">O nome do grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-118">The name of the action group.</span></span>

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

### <span data-ttu-id="e4f6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4f6b-120">O grupo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e4f6b-120">The resource group nam</span></span>

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

### <span data-ttu-id="e4f6b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4f6b-121">-ResourceId</span></span>
<span data-ttu-id="e4f6b-122">O recurso i</span><span class="sxs-lookup"><span data-stu-id="e4f6b-122">The resource i</span></span>

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

### <span data-ttu-id="e4f6b-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4f6b-123">-Confirm</span></span>
<span data-ttu-id="e4f6b-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f6b-125">-WhatIf</span></span>
<span data-ttu-id="e4f6b-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4f6b-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f6b-128">CommonParameters</span></span>
<span data-ttu-id="e4f6b-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f6b-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f6b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f6b-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4f6b-131">INPUTS</span></span>

### <span data-ttu-id="e4f6b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f6b-132">System.String</span></span>

### <span data-ttu-id="e4f6b-133">Microsoft. Azure. Commands. insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e4f6b-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="e4f6b-134">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4f6b-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e4f6b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4f6b-135">OUTPUTS</span></span>

### <span data-ttu-id="e4f6b-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4f6b-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e4f6b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4f6b-137">NOTES</span></span>

## <span data-ttu-id="e4f6b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4f6b-138">RELATED LINKS</span></span>

<span data-ttu-id="e4f6b-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e4f6b-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
