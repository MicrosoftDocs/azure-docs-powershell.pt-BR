---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116843"
---
# <span data-ttu-id="41790-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="41790-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="41790-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41790-102">SYNOPSIS</span></span>
<span data-ttu-id="41790-103">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="41790-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="41790-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41790-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="41790-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="41790-105">DESCRIPTION</span></span>
<span data-ttu-id="41790-106">Obter as informações de registro da área de trabalho virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="41790-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="41790-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41790-107">EXAMPLES</span></span>

### <span data-ttu-id="41790-108">Exemplo 1: Obter um Token de Registro da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="41790-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="41790-109">Esse comando obtém um Token de Registro da Área de Trabalho Virtual do Windows em um Pool de Host.</span><span class="sxs-lookup"><span data-stu-id="41790-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="41790-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41790-110">PARAMETERS</span></span>

### <span data-ttu-id="41790-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41790-111">-DefaultProfile</span></span>
<span data-ttu-id="41790-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41790-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41790-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="41790-113">-HostPoolName</span></span>
<span data-ttu-id="41790-114">Nome do pool de host</span><span class="sxs-lookup"><span data-stu-id="41790-114">Host Pool Name</span></span>

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

### <span data-ttu-id="41790-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41790-115">-ResourceGroupName</span></span>
<span data-ttu-id="41790-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="41790-116">Resource Group Name</span></span>

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

### <span data-ttu-id="41790-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41790-117">-SubscriptionId</span></span>
<span data-ttu-id="41790-118">ID da assinatura</span><span class="sxs-lookup"><span data-stu-id="41790-118">Subscription Id</span></span>

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

### <span data-ttu-id="41790-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41790-119">CommonParameters</span></span>
<span data-ttu-id="41790-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41790-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41790-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41790-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41790-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="41790-122">INPUTS</span></span>

## <span data-ttu-id="41790-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="41790-123">OUTPUTS</span></span>

### <span data-ttu-id="41790-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="41790-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="41790-125">Notas</span><span class="sxs-lookup"><span data-stu-id="41790-125">NOTES</span></span>

<span data-ttu-id="41790-126">Aliases</span><span class="sxs-lookup"><span data-stu-id="41790-126">ALIASES</span></span>

## <span data-ttu-id="41790-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41790-127">RELATED LINKS</span></span>

