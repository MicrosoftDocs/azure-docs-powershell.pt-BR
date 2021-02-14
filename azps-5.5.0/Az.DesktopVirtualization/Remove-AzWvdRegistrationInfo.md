---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115825"
---
# <span data-ttu-id="db643-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="db643-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="db643-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db643-102">SYNOPSIS</span></span>
<span data-ttu-id="db643-103">Remover as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="db643-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="db643-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db643-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db643-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="db643-105">DESCRIPTION</span></span>
<span data-ttu-id="db643-106">Remover as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="db643-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="db643-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db643-107">EXAMPLES</span></span>

### <span data-ttu-id="db643-108">Exemplo 1: Excluir um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="db643-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="db643-109">Esse comando exclui um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="db643-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="db643-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db643-110">PARAMETERS</span></span>

### <span data-ttu-id="db643-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db643-111">-DefaultProfile</span></span>
<span data-ttu-id="db643-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db643-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db643-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="db643-113">-HostPoolName</span></span>
<span data-ttu-id="db643-114">Nome do pool de host</span><span class="sxs-lookup"><span data-stu-id="db643-114">Host Pool Name</span></span>

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

### <span data-ttu-id="db643-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db643-115">-ResourceGroupName</span></span>
<span data-ttu-id="db643-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="db643-116">Resource Group Name</span></span>

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

### <span data-ttu-id="db643-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db643-117">-SubscriptionId</span></span>
<span data-ttu-id="db643-118">ajuda foo 1</span><span class="sxs-lookup"><span data-stu-id="db643-118">help foo 1</span></span>

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

### <span data-ttu-id="db643-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="db643-119">-Confirm</span></span>
<span data-ttu-id="db643-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db643-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db643-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db643-121">-WhatIf</span></span>
<span data-ttu-id="db643-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="db643-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db643-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db643-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db643-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db643-124">CommonParameters</span></span>
<span data-ttu-id="db643-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db643-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db643-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db643-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db643-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="db643-127">INPUTS</span></span>

## <span data-ttu-id="db643-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="db643-128">OUTPUTS</span></span>

## <span data-ttu-id="db643-129">Notas</span><span class="sxs-lookup"><span data-stu-id="db643-129">NOTES</span></span>

<span data-ttu-id="db643-130">Aliases</span><span class="sxs-lookup"><span data-stu-id="db643-130">ALIASES</span></span>

## <span data-ttu-id="db643-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db643-131">RELATED LINKS</span></span>

