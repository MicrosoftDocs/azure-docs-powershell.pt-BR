---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429754"
---
# <span data-ttu-id="482e5-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="482e5-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="482e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="482e5-102">SYNOPSIS</span></span>
<span data-ttu-id="482e5-103">Obtém uma definição de Registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="482e5-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="482e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="482e5-104">SYNTAX</span></span>

### <span data-ttu-id="482e5-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="482e5-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="482e5-106">Assume</span><span class="sxs-lookup"><span data-stu-id="482e5-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="482e5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="482e5-107">DESCRIPTION</span></span>
<span data-ttu-id="482e5-108">Obtém uma definição de Registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="482e5-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="482e5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="482e5-109">EXAMPLES</span></span>

### <span data-ttu-id="482e5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="482e5-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="482e5-111">Obtém todas as definições de registro no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="482e5-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="482e5-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="482e5-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="482e5-113">Obtém a definição de registro por nome no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="482e5-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="482e5-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="482e5-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="482e5-115">Obtém todas as definições de registro em determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="482e5-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="482e5-116">OS</span><span class="sxs-lookup"><span data-stu-id="482e5-116">PARAMETERS</span></span>

### <span data-ttu-id="482e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482e5-117">-DefaultProfile</span></span>
<span data-ttu-id="482e5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="482e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="482e5-119">-Name</span></span>
<span data-ttu-id="482e5-120">O nome exclusivo da definição de registro.</span><span class="sxs-lookup"><span data-stu-id="482e5-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e5-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="482e5-121">-Scope</span></span>
<span data-ttu-id="482e5-122">O escopo em que a definição de registro foi criada.</span><span class="sxs-lookup"><span data-stu-id="482e5-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="482e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482e5-123">CommonParameters</span></span>
<span data-ttu-id="482e5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="482e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482e5-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="482e5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482e5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="482e5-126">INPUTS</span></span>

### <span data-ttu-id="482e5-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="482e5-127">None</span></span>
## <span data-ttu-id="482e5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="482e5-128">OUTPUTS</span></span>

### <span data-ttu-id="482e5-129">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="482e5-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="482e5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="482e5-130">NOTES</span></span>

## <span data-ttu-id="482e5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="482e5-131">RELATED LINKS</span></span>
