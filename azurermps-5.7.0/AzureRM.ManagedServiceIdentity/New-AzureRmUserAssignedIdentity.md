---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/new-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/New-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 9f4bea5ce1eaad0096ed36628704d9406047d5f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430996"
---
# <span data-ttu-id="fcf36-101">New-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fcf36-101">New-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="fcf36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcf36-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf36-103">Cria uma nova identidade atribuída ao usuário ou atualiza uma identidade atribuída pelo usuário existente.</span><span class="sxs-lookup"><span data-stu-id="fcf36-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcf36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcf36-104">SYNTAX</span></span>

```
New-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf36-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcf36-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf36-106">O cmdlet **New-AzureRmUserAssignedIdentity** cria uma nova identidade atribuída ao usuário.</span><span class="sxs-lookup"><span data-stu-id="fcf36-106">The **New-AzureRmUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="fcf36-107">Quando usado com uma identidade já existente, ele atualizou a identidade.</span><span class="sxs-lookup"><span data-stu-id="fcf36-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="fcf36-108">Para adicionar marcas do Azure Resource Manager à identidade, use o cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="fcf36-108">To add Azure Resource Manager tags to the identity, please use the Set-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="fcf36-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcf36-109">EXAMPLES</span></span>

### <span data-ttu-id="fcf36-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fcf36-110">Example 1</span></span>
<span data-ttu-id="fcf36-111">Este cmdlet de exemplo cria uma nova identidade atribuída ao usuário com o nome **ID1** em **PSRG** do grupo de recursos no local do grupo de Resource.</span><span class="sxs-lookup"><span data-stu-id="fcf36-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="fcf36-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fcf36-112">Example 2</span></span>
<span data-ttu-id="fcf36-113">Este cmdlet de exemplo cria uma nova identidade atribuída ao usuário com o nome **ID1** abaixo do grupo de recursos **PSRG** na região oeste.</span><span class="sxs-lookup"><span data-stu-id="fcf36-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzureRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="fcf36-114">OS</span><span class="sxs-lookup"><span data-stu-id="fcf36-114">PARAMETERS</span></span>

### <span data-ttu-id="fcf36-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcf36-115">-AsJob</span></span>
<span data-ttu-id="fcf36-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fcf36-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf36-117">-DefaultProfile</span></span>
<span data-ttu-id="fcf36-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf36-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-119">-Local</span><span class="sxs-lookup"><span data-stu-id="fcf36-119">-Location</span></span>
<span data-ttu-id="fcf36-120">O nome da região do Azure em que a identidade deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="fcf36-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fcf36-121">-Name</span></span>
<span data-ttu-id="fcf36-122">O nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="fcf36-122">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf36-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcf36-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fcf36-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="fcf36-125">-Tag</span></span>
<span data-ttu-id="fcf36-126">As marcas do Azure Resource Manager associadas à identidade.</span><span class="sxs-lookup"><span data-stu-id="fcf36-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcf36-127">-Confirm</span></span>
<span data-ttu-id="fcf36-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf36-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf36-129">-WhatIf</span></span>
<span data-ttu-id="fcf36-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcf36-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf36-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcf36-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf36-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf36-132">CommonParameters</span></span>
<span data-ttu-id="fcf36-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf36-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf36-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf36-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf36-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcf36-135">INPUTS</span></span>

### <span data-ttu-id="fcf36-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fcf36-136">None</span></span>

## <span data-ttu-id="fcf36-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcf36-137">OUTPUTS</span></span>

### <span data-ttu-id="fcf36-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fcf36-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="fcf36-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcf36-139">NOTES</span></span>

## <span data-ttu-id="fcf36-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcf36-140">RELATED LINKS</span></span>
