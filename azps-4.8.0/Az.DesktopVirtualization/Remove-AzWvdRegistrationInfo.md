---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdRegistrationInfo.md
ms.openlocfilehash: bdef7b776d8da82a357d535ff91298a2f49e9e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112260"
---
# <span data-ttu-id="9fe78-101">Remove-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="9fe78-101">Remove-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="9fe78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fe78-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe78-103">Remova as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fe78-103">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="9fe78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fe78-104">SYNTAX</span></span>

```
Remove-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9fe78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fe78-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe78-106">Remova as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fe78-106">Remove the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="9fe78-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fe78-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe78-108">Exemplo 1: excluir um token de registro da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="9fe78-108">Example 1: Delete a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Remove-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName
```

<span data-ttu-id="9fe78-109">Este comando exclui um token de registro da área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="9fe78-109">This command deletes a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="9fe78-110">OS</span><span class="sxs-lookup"><span data-stu-id="9fe78-110">PARAMETERS</span></span>

### <span data-ttu-id="9fe78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe78-111">-DefaultProfile</span></span>
<span data-ttu-id="9fe78-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe78-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="9fe78-113">-HostPoolName</span></span>
<span data-ttu-id="9fe78-114">Nome do pool do host</span><span class="sxs-lookup"><span data-stu-id="9fe78-114">Host Pool Name</span></span>

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

### <span data-ttu-id="9fe78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe78-115">-ResourceGroupName</span></span>
<span data-ttu-id="9fe78-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="9fe78-116">Resource Group Name</span></span>

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

### <span data-ttu-id="9fe78-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fe78-117">-SubscriptionId</span></span>
<span data-ttu-id="9fe78-118">ajuda do Foo 1</span><span class="sxs-lookup"><span data-stu-id="9fe78-118">help foo 1</span></span>

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

### <span data-ttu-id="9fe78-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9fe78-119">-Confirm</span></span>
<span data-ttu-id="9fe78-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe78-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe78-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe78-121">-WhatIf</span></span>
<span data-ttu-id="9fe78-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9fe78-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe78-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fe78-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe78-124">CommonParameters</span></span>
<span data-ttu-id="9fe78-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe78-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fe78-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe78-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fe78-127">INPUTS</span></span>

## <span data-ttu-id="9fe78-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fe78-128">OUTPUTS</span></span>

## <span data-ttu-id="9fe78-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fe78-129">NOTES</span></span>

<span data-ttu-id="9fe78-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9fe78-130">ALIASES</span></span>

## <span data-ttu-id="9fe78-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fe78-131">RELATED LINKS</span></span>

