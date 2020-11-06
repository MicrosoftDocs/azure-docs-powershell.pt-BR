---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430060"
---
# <span data-ttu-id="699ac-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="699ac-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="699ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="699ac-102">SYNOPSIS</span></span>
<span data-ttu-id="699ac-103">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="699ac-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="699ac-104">SYNTAX</span></span>

### <span data-ttu-id="699ac-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="699ac-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="699ac-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="699ac-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="699ac-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="699ac-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="699ac-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="699ac-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="699ac-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="699ac-109">DESCRIPTION</span></span>
<span data-ttu-id="699ac-110">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="699ac-110">Filters active directory groups.</span></span>

## <span data-ttu-id="699ac-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="699ac-111">EXAMPLES</span></span>

### <span data-ttu-id="699ac-112">Exemplo 1-listar todos os grupos do anúncio</span><span class="sxs-lookup"><span data-stu-id="699ac-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="699ac-113">Lista todos os grupos de anúncios em um locatário.</span><span class="sxs-lookup"><span data-stu-id="699ac-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="699ac-114">Exemplo 2-listar todos os grupos do AD usando paginação</span><span class="sxs-lookup"><span data-stu-id="699ac-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="699ac-115">Lista os primeiros grupos de anúncios do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="699ac-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="699ac-116">Exemplo 3-obter o grupo AD por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="699ac-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="699ac-117">Obtém um grupo de anúncios com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE '.</span><span class="sxs-lookup"><span data-stu-id="699ac-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="699ac-118">Exemplo de 4-listar grupos por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="699ac-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="699ac-119">Lista todos os grupos de anúncios cujo nome para exibição começa com ' Joe '.</span><span class="sxs-lookup"><span data-stu-id="699ac-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="699ac-120">OS</span><span class="sxs-lookup"><span data-stu-id="699ac-120">PARAMETERS</span></span>

### <span data-ttu-id="699ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699ac-121">-DefaultProfile</span></span>
<span data-ttu-id="699ac-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="699ac-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="699ac-123">-DisplayName</span></span>
<span data-ttu-id="699ac-124">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="699ac-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="699ac-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="699ac-126">Usado para localizar grupos que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="699ac-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-127">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="699ac-127">-First</span></span>
<span data-ttu-id="699ac-128">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="699ac-128">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="699ac-129">-IncludeTotalCount</span></span>
<span data-ttu-id="699ac-130">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="699ac-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="699ac-131">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="699ac-131">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="699ac-132">-ObjectId</span></span>
<span data-ttu-id="699ac-133">ID de objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="699ac-133">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="699ac-134">-Skip</span></span>
<span data-ttu-id="699ac-135">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="699ac-135">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ac-136">CommonParameters</span></span>
<span data-ttu-id="699ac-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ac-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699ac-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ac-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="699ac-139">INPUTS</span></span>

### <span data-ttu-id="699ac-140">System. String</span><span class="sxs-lookup"><span data-stu-id="699ac-140">System.String</span></span>

### <span data-ttu-id="699ac-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="699ac-141">System.Guid</span></span>

## <span data-ttu-id="699ac-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="699ac-142">OUTPUTS</span></span>

### <span data-ttu-id="699ac-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="699ac-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="699ac-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="699ac-144">NOTES</span></span>

## <span data-ttu-id="699ac-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="699ac-145">RELATED LINKS</span></span>

[<span data-ttu-id="699ac-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="699ac-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="699ac-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="699ac-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="699ac-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="699ac-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

