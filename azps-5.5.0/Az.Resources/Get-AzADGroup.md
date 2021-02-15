---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111443"
---
# <span data-ttu-id="3bf62-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="3bf62-101">Get-AzADGroup</span></span>

## <span data-ttu-id="3bf62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bf62-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf62-103">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3bf62-103">Filters active directory groups.</span></span>

## <span data-ttu-id="3bf62-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bf62-104">SYNTAX</span></span>

### <span data-ttu-id="3bf62-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3bf62-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3bf62-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf62-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3bf62-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf62-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3bf62-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bf62-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="3bf62-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bf62-109">DESCRIPTION</span></span>
<span data-ttu-id="3bf62-110">Filtra grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3bf62-110">Filters active directory groups.</span></span>

## <span data-ttu-id="3bf62-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bf62-111">EXAMPLES</span></span>

### <span data-ttu-id="3bf62-112">Exemplo 1: Listar todos os grupos de AD</span><span class="sxs-lookup"><span data-stu-id="3bf62-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="3bf62-113">Lista todos os grupos de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="3bf62-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="3bf62-114">Exemplo 2: Listar todos os grupos de AD usando paging</span><span class="sxs-lookup"><span data-stu-id="3bf62-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="3bf62-115">Lista os primeiros 100 grupos de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="3bf62-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="3bf62-116">Exemplo 3: Obter grupo AD por id de objeto</span><span class="sxs-lookup"><span data-stu-id="3bf62-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3bf62-117">Obtém um grupo AD com a ID do objeto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="3bf62-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="3bf62-118">Exemplo 4: Listar grupos por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="3bf62-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="3bf62-119">Lista todos os grupos de AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="3bf62-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="3bf62-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bf62-120">PARAMETERS</span></span>

### <span data-ttu-id="3bf62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf62-121">-DefaultProfile</span></span>
<span data-ttu-id="3bf62-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3bf62-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bf62-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bf62-123">-DisplayName</span></span>
<span data-ttu-id="3bf62-124">O nome de exibição do grupo.</span><span class="sxs-lookup"><span data-stu-id="3bf62-124">The display name of the group.</span></span>

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

### <span data-ttu-id="3bf62-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="3bf62-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="3bf62-126">Usado para encontrar grupos que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="3bf62-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="3bf62-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3bf62-127">-ObjectId</span></span>
<span data-ttu-id="3bf62-128">ID do objeto do grupo.</span><span class="sxs-lookup"><span data-stu-id="3bf62-128">Object id of the group.</span></span>

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

### <span data-ttu-id="3bf62-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3bf62-129">-IncludeTotalCount</span></span>
<span data-ttu-id="3bf62-130">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="3bf62-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="3bf62-131">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="3bf62-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="3bf62-132">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="3bf62-132">-Skip</span></span>
<span data-ttu-id="3bf62-133">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="3bf62-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="3bf62-134">-First</span><span class="sxs-lookup"><span data-stu-id="3bf62-134">-First</span></span>
<span data-ttu-id="3bf62-135">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="3bf62-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="3bf62-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf62-136">CommonParameters</span></span>
<span data-ttu-id="3bf62-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf62-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf62-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bf62-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf62-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="3bf62-139">INPUTS</span></span>

### <span data-ttu-id="3bf62-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3bf62-140">System.String</span></span>

### <span data-ttu-id="3bf62-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3bf62-141">System.Guid</span></span>

## <span data-ttu-id="3bf62-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="3bf62-142">OUTPUTS</span></span>

### <span data-ttu-id="3bf62-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3bf62-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3bf62-144">Notas</span><span class="sxs-lookup"><span data-stu-id="3bf62-144">NOTES</span></span>

## <span data-ttu-id="3bf62-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bf62-145">RELATED LINKS</span></span>

[<span data-ttu-id="3bf62-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="3bf62-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="3bf62-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3bf62-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="3bf62-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="3bf62-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

