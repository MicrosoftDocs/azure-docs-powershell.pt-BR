---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886597"
---
# <span data-ttu-id="7c8e4-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7c8e4-101">Get-AzADUser</span></span>

## <span data-ttu-id="7c8e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8e4-103">Filtra os usuários do active directory.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-103">Filters active directory users.</span></span>

## <span data-ttu-id="7c8e4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c8e4-104">SYNTAX</span></span>

### <span data-ttu-id="7c8e4-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c8e4-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7c8e4-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8e4-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7c8e4-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8e4-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7c8e4-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8e4-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7c8e4-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8e4-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7c8e4-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c8e4-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7c8e4-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c8e4-111">DESCRIPTION</span></span>
<span data-ttu-id="7c8e4-112">Filtra os usuários do active directory.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-112">Filters active directory users.</span></span>

## <span data-ttu-id="7c8e4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-113">EXAMPLES</span></span>

### <span data-ttu-id="7c8e4-114">Exemplo 1: Listar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="7c8e4-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="7c8e4-115">Lista todos os usuários do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="7c8e4-116">Exemplo 2: Listar todos os usuários usando paging</span><span class="sxs-lookup"><span data-stu-id="7c8e4-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="7c8e4-117">Lista os primeiros 100 usuários do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="7c8e4-118">Exemplo 3: Obter usuário do AD pelo nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="7c8e4-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="7c8e4-119">Obtém o usuário do AD com o nome principal do usuário " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="7c8e4-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="7c8e4-120">Exemplo 4: Lista por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="7c8e4-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="7c8e4-121">Lista todos os usuários do AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="7c8e4-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="7c8e4-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-122">PARAMETERS</span></span>

### <span data-ttu-id="7c8e4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8e4-123">-DefaultProfile</span></span>
<span data-ttu-id="7c8e4-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7c8e4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c8e4-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7c8e4-125">-DisplayName</span></span>
<span data-ttu-id="7c8e4-126">O nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-126">The display name of the user.</span></span>

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

### <span data-ttu-id="7c8e4-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="7c8e4-127">-Mail</span></span>
<span data-ttu-id="7c8e4-128">O email do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8e4-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7c8e4-129">-ObjectId</span></span>
<span data-ttu-id="7c8e4-130">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8e4-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="7c8e4-131">-StartsWith</span></span>
<span data-ttu-id="7c8e4-132">Usado para encontrar usuários que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="7c8e4-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7c8e4-133">-UserPrincipalName</span></span>
<span data-ttu-id="7c8e4-134">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8e4-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7c8e4-135">-IncludeTotalCount</span></span>
<span data-ttu-id="7c8e4-136">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7c8e4-137">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7c8e4-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="7c8e4-138">-Skip</span></span>
<span data-ttu-id="7c8e4-139">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="7c8e4-140">-First</span><span class="sxs-lookup"><span data-stu-id="7c8e4-140">-First</span></span>
<span data-ttu-id="7c8e4-141">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="7c8e4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8e4-142">CommonParameters</span></span>
<span data-ttu-id="7c8e4-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8e4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8e4-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c8e4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8e4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-145">INPUTS</span></span>

### <span data-ttu-id="7c8e4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7c8e4-146">System.String</span></span>

## <span data-ttu-id="7c8e4-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-147">OUTPUTS</span></span>

### <span data-ttu-id="7c8e4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="7c8e4-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7c8e4-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c8e4-149">NOTES</span></span>

## <span data-ttu-id="7c8e4-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c8e4-150">RELATED LINKS</span></span>

[<span data-ttu-id="7c8e4-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7c8e4-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="7c8e4-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7c8e4-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="7c8e4-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7c8e4-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

