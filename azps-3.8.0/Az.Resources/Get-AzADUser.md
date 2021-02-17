---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 80df38532d5d5ce14b27f40bed04678e80752fca
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406988"
---
# <span data-ttu-id="5f841-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5f841-101">Get-AzADUser</span></span>

## <span data-ttu-id="5f841-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f841-102">SYNOPSIS</span></span>
<span data-ttu-id="5f841-103">Filtra os usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f841-103">Filters active directory users.</span></span>

## <span data-ttu-id="5f841-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f841-104">SYNTAX</span></span>

### <span data-ttu-id="5f841-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5f841-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f841-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f841-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f841-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f841-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f841-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f841-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f841-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f841-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5f841-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f841-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5f841-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f841-111">DESCRIPTION</span></span>
<span data-ttu-id="5f841-112">Filtra os usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f841-112">Filters active directory users.</span></span>

## <span data-ttu-id="5f841-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f841-113">EXAMPLES</span></span>

### <span data-ttu-id="5f841-114">Exemplo 1 - Listar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="5f841-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="5f841-115">Lista todos os usuários de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="5f841-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="5f841-116">Exemplo 2 - Listar todos os usuários que usam paging</span><span class="sxs-lookup"><span data-stu-id="5f841-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="5f841-117">Lista os primeiros 100 usuários de AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="5f841-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="5f841-118">Exemplo 3 - Obter usuário de AD por nome de entidade de usuário</span><span class="sxs-lookup"><span data-stu-id="5f841-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="5f841-119">Obtém o usuário do AD com o nome de usuário principal " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="5f841-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="5f841-120">Exemplo 4 - Lista por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="5f841-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="5f841-121">Lista todos os usuários do AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="5f841-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="5f841-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f841-122">PARAMETERS</span></span>

### <span data-ttu-id="5f841-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f841-123">-DefaultProfile</span></span>
<span data-ttu-id="5f841-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5f841-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f841-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f841-125">-DisplayName</span></span>
<span data-ttu-id="5f841-126">O nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f841-126">The display name of the user.</span></span>

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

### <span data-ttu-id="5f841-127">-Email</span><span class="sxs-lookup"><span data-stu-id="5f841-127">-Mail</span></span>
<span data-ttu-id="5f841-128">O email do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f841-128">The user mail.</span></span>

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

### <span data-ttu-id="5f841-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5f841-129">-ObjectId</span></span>
<span data-ttu-id="5f841-130">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f841-130">Object id of the user.</span></span>

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

### <span data-ttu-id="5f841-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="5f841-131">-StartsWith</span></span>
<span data-ttu-id="5f841-132">Usado para encontrar usuários que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="5f841-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="5f841-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f841-133">-UserPrincipalName</span></span>
<span data-ttu-id="5f841-134">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f841-134">UPN of the user.</span></span>

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

### <span data-ttu-id="5f841-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5f841-135">-IncludeTotalCount</span></span>
<span data-ttu-id="5f841-136">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="5f841-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5f841-137">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="5f841-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5f841-138">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="5f841-138">-Skip</span></span>
<span data-ttu-id="5f841-139">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="5f841-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5f841-140">-First</span><span class="sxs-lookup"><span data-stu-id="5f841-140">-First</span></span>
<span data-ttu-id="5f841-141">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="5f841-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5f841-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f841-142">CommonParameters</span></span>
<span data-ttu-id="5f841-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f841-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f841-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f841-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f841-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="5f841-145">INPUTS</span></span>

### <span data-ttu-id="5f841-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5f841-146">System.String</span></span>

## <span data-ttu-id="5f841-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="5f841-147">OUTPUTS</span></span>

### <span data-ttu-id="5f841-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="5f841-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="5f841-149">Notas</span><span class="sxs-lookup"><span data-stu-id="5f841-149">NOTES</span></span>

## <span data-ttu-id="5f841-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f841-150">RELATED LINKS</span></span>

[<span data-ttu-id="5f841-151">Novo-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5f841-151">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="5f841-152">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5f841-152">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

