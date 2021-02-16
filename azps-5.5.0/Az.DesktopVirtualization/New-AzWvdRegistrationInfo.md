---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113233"
---
# <span data-ttu-id="ade28-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ade28-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="ade28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ade28-102">SYNOPSIS</span></span>
<span data-ttu-id="ade28-103">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="ade28-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ade28-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ade28-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ade28-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ade28-105">DESCRIPTION</span></span>
<span data-ttu-id="ade28-106">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="ade28-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="ade28-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ade28-107">EXAMPLES</span></span>

### <span data-ttu-id="ade28-108">Exemplo 1: Criar um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="ade28-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="ade28-109">Esse comando cria um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="ade28-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="ade28-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ade28-110">PARAMETERS</span></span>

### <span data-ttu-id="ade28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade28-111">-DefaultProfile</span></span>
<span data-ttu-id="ade28-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ade28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade28-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="ade28-113">-ExpirationTime</span></span>
<span data-ttu-id="ade28-114">Tempo de Expiração</span><span class="sxs-lookup"><span data-stu-id="ade28-114">Expiration Time</span></span>

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

### <span data-ttu-id="ade28-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ade28-115">-HostPoolName</span></span>
<span data-ttu-id="ade28-116">Nome do pool de host</span><span class="sxs-lookup"><span data-stu-id="ade28-116">Host Pool Name</span></span>

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

### <span data-ttu-id="ade28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade28-117">-ResourceGroupName</span></span>
<span data-ttu-id="ade28-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ade28-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ade28-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ade28-119">-SubscriptionId</span></span>
<span data-ttu-id="ade28-120">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="ade28-120">Subscription Id</span></span>

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

### <span data-ttu-id="ade28-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ade28-121">-Confirm</span></span>
<span data-ttu-id="ade28-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade28-123">-WhatIf</span></span>
<span data-ttu-id="ade28-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ade28-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade28-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ade28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade28-126">CommonParameters</span></span>
<span data-ttu-id="ade28-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade28-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade28-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="ade28-129">INPUTS</span></span>

## <span data-ttu-id="ade28-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="ade28-130">OUTPUTS</span></span>

### <span data-ttu-id="ade28-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="ade28-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="ade28-132">Notas</span><span class="sxs-lookup"><span data-stu-id="ade28-132">NOTES</span></span>

<span data-ttu-id="ade28-133">Aliases</span><span class="sxs-lookup"><span data-stu-id="ade28-133">ALIASES</span></span>

## <span data-ttu-id="ade28-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ade28-134">RELATED LINKS</span></span>

