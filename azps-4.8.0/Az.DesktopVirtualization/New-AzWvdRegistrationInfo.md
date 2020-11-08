---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115014"
---
# <span data-ttu-id="516d7-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="516d7-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="516d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="516d7-102">SYNOPSIS</span></span>
<span data-ttu-id="516d7-103">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="516d7-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="516d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="516d7-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="516d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="516d7-105">DESCRIPTION</span></span>
<span data-ttu-id="516d7-106">Criar informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="516d7-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="516d7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="516d7-107">EXAMPLES</span></span>

### <span data-ttu-id="516d7-108">Exemplo 1: criar um token de registro da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="516d7-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="516d7-109">Esse comando cria um token de registro da área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="516d7-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="516d7-110">OS</span><span class="sxs-lookup"><span data-stu-id="516d7-110">PARAMETERS</span></span>

### <span data-ttu-id="516d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="516d7-111">-DefaultProfile</span></span>
<span data-ttu-id="516d7-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="516d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="516d7-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="516d7-113">-ExpirationTime</span></span>
<span data-ttu-id="516d7-114">Tempo de expiração</span><span class="sxs-lookup"><span data-stu-id="516d7-114">Expiration Time</span></span>

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

### <span data-ttu-id="516d7-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="516d7-115">-HostPoolName</span></span>
<span data-ttu-id="516d7-116">Nome do pool do host</span><span class="sxs-lookup"><span data-stu-id="516d7-116">Host Pool Name</span></span>

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

### <span data-ttu-id="516d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="516d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="516d7-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="516d7-118">Resource Group Name</span></span>

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

### <span data-ttu-id="516d7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="516d7-119">-SubscriptionId</span></span>
<span data-ttu-id="516d7-120">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="516d7-120">Subscription Id</span></span>

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

### <span data-ttu-id="516d7-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="516d7-121">-Confirm</span></span>
<span data-ttu-id="516d7-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="516d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="516d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="516d7-123">-WhatIf</span></span>
<span data-ttu-id="516d7-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="516d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="516d7-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="516d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="516d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516d7-126">CommonParameters</span></span>
<span data-ttu-id="516d7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="516d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516d7-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="516d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516d7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="516d7-129">INPUTS</span></span>

## <span data-ttu-id="516d7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="516d7-130">OUTPUTS</span></span>

### <span data-ttu-id="516d7-131">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="516d7-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="516d7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="516d7-132">NOTES</span></span>

<span data-ttu-id="516d7-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="516d7-133">ALIASES</span></span>

## <span data-ttu-id="516d7-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="516d7-134">RELATED LINKS</span></span>

