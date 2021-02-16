---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398726"
---
# <span data-ttu-id="68dff-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="68dff-101">Get-AzADUser</span></span>

## <span data-ttu-id="68dff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68dff-102">SYNOPSIS</span></span>
<span data-ttu-id="68dff-103">Filtra os usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68dff-103">Filters active directory users.</span></span>

## <span data-ttu-id="68dff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68dff-104">SYNTAX</span></span>

### <span data-ttu-id="68dff-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="68dff-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="68dff-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="68dff-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="68dff-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="68dff-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="68dff-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68dff-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="68dff-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="68dff-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="68dff-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="68dff-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="68dff-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="68dff-111">DESCRIPTION</span></span>
<span data-ttu-id="68dff-112">Filtra os usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68dff-112">Filters active directory users.</span></span>

## <span data-ttu-id="68dff-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68dff-113">EXAMPLES</span></span>

### <span data-ttu-id="68dff-114">Exemplo 1 - Listar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="68dff-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="68dff-115">Lista todos os usuários de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="68dff-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="68dff-116">Exemplo 2 - Listar todos os usuários que usam paging</span><span class="sxs-lookup"><span data-stu-id="68dff-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="68dff-117">Lista os primeiros 100 usuários de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="68dff-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="68dff-118">Exemplo 3 - Obter usuário de AD por nome de entidade de usuário</span><span class="sxs-lookup"><span data-stu-id="68dff-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="68dff-119">Obtém o usuário do AD com o nome de usuário principal " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="68dff-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="68dff-120">Exemplo 4 - Lista por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="68dff-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="68dff-121">Lista todos os usuários do AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="68dff-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="68dff-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68dff-122">PARAMETERS</span></span>

### <span data-ttu-id="68dff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68dff-123">-DefaultProfile</span></span>
<span data-ttu-id="68dff-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="68dff-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68dff-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68dff-125">-DisplayName</span></span>
<span data-ttu-id="68dff-126">O nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="68dff-126">The display name of the user.</span></span>

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

### <span data-ttu-id="68dff-127">-First</span><span class="sxs-lookup"><span data-stu-id="68dff-127">-First</span></span>
<span data-ttu-id="68dff-128">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="68dff-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="68dff-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="68dff-129">-IncludeTotalCount</span></span>
<span data-ttu-id="68dff-130">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="68dff-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="68dff-131">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="68dff-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="68dff-132">-Email</span><span class="sxs-lookup"><span data-stu-id="68dff-132">-Mail</span></span>
<span data-ttu-id="68dff-133">O email do usuário.</span><span class="sxs-lookup"><span data-stu-id="68dff-133">The user mail.</span></span>

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

### <span data-ttu-id="68dff-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="68dff-134">-ObjectId</span></span>
<span data-ttu-id="68dff-135">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="68dff-135">Object id of the user.</span></span>

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

### <span data-ttu-id="68dff-136">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="68dff-136">-Skip</span></span>
<span data-ttu-id="68dff-137">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="68dff-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="68dff-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="68dff-138">-StartsWith</span></span>
<span data-ttu-id="68dff-139">Usado para encontrar usuários que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="68dff-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="68dff-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="68dff-140">-UserPrincipalName</span></span>
<span data-ttu-id="68dff-141">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="68dff-141">UPN of the user.</span></span>

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

### <span data-ttu-id="68dff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dff-142">CommonParameters</span></span>
<span data-ttu-id="68dff-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68dff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dff-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68dff-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dff-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="68dff-145">INPUTS</span></span>

### <span data-ttu-id="68dff-146">System.String</span><span class="sxs-lookup"><span data-stu-id="68dff-146">System.String</span></span>

### <span data-ttu-id="68dff-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="68dff-147">System.Guid</span></span>

## <span data-ttu-id="68dff-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="68dff-148">OUTPUTS</span></span>

### <span data-ttu-id="68dff-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="68dff-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="68dff-150">Notas</span><span class="sxs-lookup"><span data-stu-id="68dff-150">NOTES</span></span>

## <span data-ttu-id="68dff-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68dff-151">RELATED LINKS</span></span>

[<span data-ttu-id="68dff-152">Novo-AzADUser</span><span class="sxs-lookup"><span data-stu-id="68dff-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="68dff-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="68dff-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

