---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 80c315b5bb2e1a1bcd15a2b9686a1201739171a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892961"
---
# <span data-ttu-id="630e6-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="630e6-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="630e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="630e6-102">SYNOPSIS</span></span>
<span data-ttu-id="630e6-103">Obtém uma definição de registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="630e6-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="630e6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="630e6-104">SYNTAX</span></span>

### <span data-ttu-id="630e6-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="630e6-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="630e6-106">Padrão</span><span class="sxs-lookup"><span data-stu-id="630e6-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="630e6-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="630e6-107">DESCRIPTION</span></span>
<span data-ttu-id="630e6-108">Obtém uma definição de registro específica ou uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="630e6-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="630e6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="630e6-109">EXAMPLES</span></span>

### <span data-ttu-id="630e6-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="630e6-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="630e6-111">Obtém todas as definições de registro no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="630e6-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="630e6-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="630e6-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="630e6-113">Obtém a definição de registro por nome no escopo padrão.</span><span class="sxs-lookup"><span data-stu-id="630e6-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="630e6-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="630e6-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="630e6-115">Obtém todas as definições de registro no escopo determinado.</span><span class="sxs-lookup"><span data-stu-id="630e6-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="630e6-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="630e6-116">PARAMETERS</span></span>

### <span data-ttu-id="630e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630e6-117">-DefaultProfile</span></span>
<span data-ttu-id="630e6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="630e6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="630e6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="630e6-119">-Name</span></span>
<span data-ttu-id="630e6-120">O nome exclusivo da Definição de Registro.</span><span class="sxs-lookup"><span data-stu-id="630e6-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="630e6-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="630e6-121">-Scope</span></span>
<span data-ttu-id="630e6-122">O escopo em que a definição de registro foi criada.</span><span class="sxs-lookup"><span data-stu-id="630e6-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="630e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630e6-123">CommonParameters</span></span>
<span data-ttu-id="630e6-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630e6-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="630e6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630e6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="630e6-126">INPUTS</span></span>

### <span data-ttu-id="630e6-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="630e6-127">None</span></span>
## <span data-ttu-id="630e6-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="630e6-128">OUTPUTS</span></span>

### <span data-ttu-id="630e6-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="630e6-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="630e6-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="630e6-130">NOTES</span></span>

## <span data-ttu-id="630e6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="630e6-131">RELATED LINKS</span></span>
