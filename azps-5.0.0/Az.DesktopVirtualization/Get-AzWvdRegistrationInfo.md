---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280571"
---
# <span data-ttu-id="4b825-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4b825-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="4b825-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b825-102">SYNOPSIS</span></span>
<span data-ttu-id="4b825-103">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b825-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4b825-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b825-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4b825-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b825-105">DESCRIPTION</span></span>
<span data-ttu-id="4b825-106">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="4b825-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="4b825-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b825-107">EXAMPLES</span></span>

### <span data-ttu-id="4b825-108">Exemplo 1: obter um token de registro da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="4b825-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="4b825-109">Este comando obtém um token de registro da área de trabalho virtual do Windows em um pool de hosts.</span><span class="sxs-lookup"><span data-stu-id="4b825-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="4b825-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b825-110">PARAMETERS</span></span>

### <span data-ttu-id="4b825-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b825-111">-DefaultProfile</span></span>
<span data-ttu-id="4b825-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b825-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b825-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4b825-113">-HostPoolName</span></span>
<span data-ttu-id="4b825-114">Nome do pool do host</span><span class="sxs-lookup"><span data-stu-id="4b825-114">Host Pool Name</span></span>

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

### <span data-ttu-id="4b825-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b825-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b825-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b825-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4b825-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b825-117">-SubscriptionId</span></span>
<span data-ttu-id="4b825-118">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="4b825-118">Subscription Id</span></span>

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

### <span data-ttu-id="4b825-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b825-119">CommonParameters</span></span>
<span data-ttu-id="4b825-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b825-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b825-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b825-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b825-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b825-122">INPUTS</span></span>

## <span data-ttu-id="4b825-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b825-123">OUTPUTS</span></span>

### <span data-ttu-id="4b825-124">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="4b825-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="4b825-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b825-125">NOTES</span></span>

<span data-ttu-id="4b825-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4b825-126">ALIASES</span></span>

## <span data-ttu-id="4b825-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b825-127">RELATED LINKS</span></span>

