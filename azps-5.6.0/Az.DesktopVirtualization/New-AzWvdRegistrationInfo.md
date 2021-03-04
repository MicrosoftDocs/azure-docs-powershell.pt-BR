---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887149"
---
# <span data-ttu-id="bb994-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="bb994-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="bb994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb994-102">SYNOPSIS</span></span>
<span data-ttu-id="bb994-103">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb994-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="bb994-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb994-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bb994-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb994-105">DESCRIPTION</span></span>
<span data-ttu-id="bb994-106">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb994-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="bb994-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb994-107">EXAMPLES</span></span>

### <span data-ttu-id="bb994-108">Exemplo 1: Criar um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="bb994-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="bb994-109">Este comando cria um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="bb994-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="bb994-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb994-110">PARAMETERS</span></span>

### <span data-ttu-id="bb994-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb994-111">-DefaultProfile</span></span>
<span data-ttu-id="bb994-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb994-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb994-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="bb994-113">-ExpirationTime</span></span>
<span data-ttu-id="bb994-114">Tempo de expiração</span><span class="sxs-lookup"><span data-stu-id="bb994-114">Expiration Time</span></span>

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

### <span data-ttu-id="bb994-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="bb994-115">-HostPoolName</span></span>
<span data-ttu-id="bb994-116">Nome do Pool de Host</span><span class="sxs-lookup"><span data-stu-id="bb994-116">Host Pool Name</span></span>

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

### <span data-ttu-id="bb994-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb994-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb994-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bb994-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bb994-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb994-119">-SubscriptionId</span></span>
<span data-ttu-id="bb994-120">Id da assinatura</span><span class="sxs-lookup"><span data-stu-id="bb994-120">Subscription Id</span></span>

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

### <span data-ttu-id="bb994-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb994-121">-Confirm</span></span>
<span data-ttu-id="bb994-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb994-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb994-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb994-123">-WhatIf</span></span>
<span data-ttu-id="bb994-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb994-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb994-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb994-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb994-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb994-126">CommonParameters</span></span>
<span data-ttu-id="bb994-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb994-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb994-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb994-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb994-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb994-129">INPUTS</span></span>

## <span data-ttu-id="bb994-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb994-130">OUTPUTS</span></span>

### <span data-ttu-id="bb994-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="bb994-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="bb994-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb994-132">NOTES</span></span>

<span data-ttu-id="bb994-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bb994-133">ALIASES</span></span>

## <span data-ttu-id="bb994-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb994-134">RELATED LINKS</span></span>

