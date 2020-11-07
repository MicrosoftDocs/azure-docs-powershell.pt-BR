---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: a4a365cdaee79a39b87331c42c832e40f7cbd657
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944198"
---
# <span data-ttu-id="6905b-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="6905b-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="6905b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6905b-102">SYNOPSIS</span></span>
<span data-ttu-id="6905b-103">Obtém uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="6905b-103">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="6905b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6905b-104">SYNTAX</span></span>

### <span data-ttu-id="6905b-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="6905b-105">Default (Default)</span></span>
```
Get-AzManagedServicesDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6905b-106">ById</span><span class="sxs-lookup"><span data-stu-id="6905b-106">ById</span></span>
```
Get-AzManagedServicesDefinition -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6905b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6905b-107">ByResourceId</span></span>
```
Get-AzManagedServicesDefinition -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6905b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6905b-108">DESCRIPTION</span></span>
<span data-ttu-id="6905b-109">Obtém uma lista das definições de registro.</span><span class="sxs-lookup"><span data-stu-id="6905b-109">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="6905b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6905b-110">EXAMPLES</span></span>

### <span data-ttu-id="6905b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6905b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition

Name                                 ManagedByTenantId                    PrincipalId                                                                  RoleDefinitionId
----                                 -----------------                    -----------                                                                  ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
ee7e40e8-bc3f-4624-b0ca-d5364635b141 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
e2ddcd3c-d50f-4d51-afd9-f9132fcae4e7 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
d3301f65-7087-438c-a6bc-4b7ead094889 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
cae481c0-de7c-42a8-86c1-5b170861caf8 bab3375b-6197-4a15-a44b-16c41faa91d7 {d6f6c88a-5b7a-455e-ba40-ce146d4d3671, d6f6c88a-5b7a-455e-ba40-ce146d4d3671} {acdd72a7-3385-48ef-bd42-f606fba81ae7, b24988ac-6180-42a0-ab88-20f7382dd24c}
bb2626be-3e11-442f-b0f1-9209508d4f52 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="6905b-112">Obtém todas as definições de registro.</span><span class="sxs-lookup"><span data-stu-id="6905b-112">Gets all registration definitions.</span></span>

### <span data-ttu-id="6905b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6905b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition -Id fff287a4-1714-4a17-bc40-a17ca8e69e3f

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="6905b-114">Obtém a definição de registro de acordo com sua ID.</span><span class="sxs-lookup"><span data-stu-id="6905b-114">Gets the registration definition given its id.</span></span>

### <span data-ttu-id="6905b-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6905b-115">Example 3</span></span>
```powershell
PS C:\> $definitions = Get-AzManagedServicesDefinition
PS C:\> $definitions[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/fff287a4-1714-4a17-bc40-a17ca8e69e3f
PS C:\> Get-AzManagedServicesDefinition -ResourceId $definitions[0].Id

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="6905b-116">Obtém a definição de registro de acordo com a ID de recurso totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="6905b-116">Gets the registration definition given the fully qualified resource id.</span></span>

## <span data-ttu-id="6905b-117">OS</span><span class="sxs-lookup"><span data-stu-id="6905b-117">PARAMETERS</span></span>

### <span data-ttu-id="6905b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6905b-118">-DefaultProfile</span></span>
<span data-ttu-id="6905b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6905b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6905b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="6905b-120">-Id</span></span>
<span data-ttu-id="6905b-121">O identificador de definição de registro (por exemplo, b0c052e5-c437-4771-a476-8b1201158a57).</span><span class="sxs-lookup"><span data-stu-id="6905b-121">The registration definition identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6905b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6905b-122">-ResourceId</span></span>
<span data-ttu-id="6905b-123">A ID de recurso totalmente qualificado da definição de registro (por exemplo,/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span><span class="sxs-lookup"><span data-stu-id="6905b-123">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6905b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6905b-124">CommonParameters</span></span>
<span data-ttu-id="6905b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6905b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6905b-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6905b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6905b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6905b-127">INPUTS</span></span>

### <span data-ttu-id="6905b-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6905b-128">None</span></span>

## <span data-ttu-id="6905b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6905b-129">OUTPUTS</span></span>

### <span data-ttu-id="6905b-130">Microsoft. Azure. PowerShell. cmdlets. Managedservices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="6905b-130">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="6905b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6905b-131">NOTES</span></span>

## <span data-ttu-id="6905b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6905b-132">RELATED LINKS</span></span>
