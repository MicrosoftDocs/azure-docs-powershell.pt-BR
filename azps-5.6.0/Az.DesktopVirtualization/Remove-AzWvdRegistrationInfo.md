---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: 548e7d19e2d5285ed4063bc9c14202980c02028d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888952"
---
# <span data-ttu-id="09e47-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="09e47-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="09e47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e47-102">SYNOPSIS</span></span>
<span data-ttu-id="09e47-103">Remova as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="09e47-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="09e47-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09e47-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09e47-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09e47-105">DESCRIPTION</span></span>
<span data-ttu-id="09e47-106">Remova as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="09e47-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="09e47-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09e47-107">EXAMPLES</span></span>

### <span data-ttu-id="09e47-108">Exemplo 1: Excluir um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="09e47-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="09e47-109">Este comando exclui um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="09e47-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="09e47-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09e47-110">PARAMETERS</span></span>

### <span data-ttu-id="09e47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e47-111">-DefaultProfile</span></span>
<span data-ttu-id="09e47-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09e47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e47-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="09e47-113">-HostPoolName</span></span>
<span data-ttu-id="09e47-114">Nome do Pool de Host</span><span class="sxs-lookup"><span data-stu-id="09e47-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e47-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e47-115">-ResourceGroupName</span></span>
<span data-ttu-id="09e47-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="09e47-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e47-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09e47-117">-SubscriptionId</span></span>
<span data-ttu-id="09e47-118">help foo 1</span><span class="sxs-lookup"><span data-stu-id="09e47-118">help foo 1</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e47-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09e47-119">-Confirm</span></span>
<span data-ttu-id="09e47-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09e47-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e47-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e47-121">-WhatIf</span></span>
<span data-ttu-id="09e47-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09e47-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e47-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09e47-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e47-124">CommonParameters</span></span>
<span data-ttu-id="09e47-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e47-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09e47-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e47-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09e47-127">INPUTS</span></span>

## <span data-ttu-id="09e47-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09e47-128">OUTPUTS</span></span>

## <span data-ttu-id="09e47-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="09e47-129">NOTES</span></span>

<span data-ttu-id="09e47-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09e47-130">ALIASES</span></span>

## <span data-ttu-id="09e47-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09e47-131">RELATED LINKS</span></span>

