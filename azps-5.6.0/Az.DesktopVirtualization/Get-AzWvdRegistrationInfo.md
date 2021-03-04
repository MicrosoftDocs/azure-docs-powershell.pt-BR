---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 868cbf6aaaf9b9c304c6afa65e63e6eca12910d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886640"
---
# <span data-ttu-id="95d0a-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="95d0a-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="95d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="95d0a-103">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="95d0a-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="95d0a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95d0a-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="95d0a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="95d0a-106">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="95d0a-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="95d0a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="95d0a-108">Exemplo 1: Obter um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="95d0a-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="95d0a-109">Este comando obtém um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="95d0a-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="95d0a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="95d0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d0a-111">-DefaultProfile</span></span>
<span data-ttu-id="95d0a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95d0a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d0a-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="95d0a-113">-HostPoolName</span></span>
<span data-ttu-id="95d0a-114">Nome do Pool de Host</span><span class="sxs-lookup"><span data-stu-id="95d0a-114">Host Pool Name</span></span>

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

### <span data-ttu-id="95d0a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d0a-115">-ResourceGroupName</span></span>
<span data-ttu-id="95d0a-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="95d0a-116">Resource Group Name</span></span>

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

### <span data-ttu-id="95d0a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95d0a-117">-SubscriptionId</span></span>
<span data-ttu-id="95d0a-118">Id da assinatura</span><span class="sxs-lookup"><span data-stu-id="95d0a-118">Subscription Id</span></span>

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

### <span data-ttu-id="95d0a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d0a-119">CommonParameters</span></span>
<span data-ttu-id="95d0a-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d0a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d0a-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d0a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d0a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95d0a-122">INPUTS</span></span>

## <span data-ttu-id="95d0a-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95d0a-123">OUTPUTS</span></span>

### <span data-ttu-id="95d0a-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="95d0a-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="95d0a-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="95d0a-125">NOTES</span></span>

<span data-ttu-id="95d0a-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="95d0a-126">ALIASES</span></span>

## <span data-ttu-id="95d0a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95d0a-127">RELATED LINKS</span></span>

