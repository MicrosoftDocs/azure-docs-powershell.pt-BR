---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776457"
---
# <span data-ttu-id="181fa-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="181fa-101">Get-AzADUser</span></span>

## <span data-ttu-id="181fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="181fa-102">SYNOPSIS</span></span>
<span data-ttu-id="181fa-103">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="181fa-103">Filters active directory users.</span></span>

## <span data-ttu-id="181fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="181fa-104">SYNTAX</span></span>

### <span data-ttu-id="181fa-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="181fa-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="181fa-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="181fa-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="181fa-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="181fa-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="181fa-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="181fa-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="181fa-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="181fa-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="181fa-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="181fa-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="181fa-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="181fa-111">DESCRIPTION</span></span>
<span data-ttu-id="181fa-112">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="181fa-112">Filters active directory users.</span></span>

## <span data-ttu-id="181fa-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="181fa-113">EXAMPLES</span></span>

### <span data-ttu-id="181fa-114">Exemplo 1-listar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="181fa-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="181fa-115">Lista todos os usuários do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="181fa-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="181fa-116">Exemplo 2-listar todos os usuários que usam paginação</span><span class="sxs-lookup"><span data-stu-id="181fa-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="181fa-117">Lista os primeiros usuários do 100 AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="181fa-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="181fa-118">Exemplo 3-obter usuário do AD por nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="181fa-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="181fa-119">Obtém o usuário do anúncio com o nome principal do usuário " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="181fa-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="181fa-120">Exemplo de 4-lista por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="181fa-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="181fa-121">Lista todos os usuários do AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="181fa-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="181fa-122">OS</span><span class="sxs-lookup"><span data-stu-id="181fa-122">PARAMETERS</span></span>

### <span data-ttu-id="181fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181fa-123">-DefaultProfile</span></span>
<span data-ttu-id="181fa-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="181fa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="181fa-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="181fa-125">-DisplayName</span></span>
<span data-ttu-id="181fa-126">O nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="181fa-126">The display name of the user.</span></span>

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

### <span data-ttu-id="181fa-127">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="181fa-127">-First</span></span>
<span data-ttu-id="181fa-128">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="181fa-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="181fa-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="181fa-129">-IncludeTotalCount</span></span>
<span data-ttu-id="181fa-130">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="181fa-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="181fa-131">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="181fa-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="181fa-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="181fa-132">-Mail</span></span>
<span data-ttu-id="181fa-133">O email do usuário.</span><span class="sxs-lookup"><span data-stu-id="181fa-133">The user mail.</span></span>

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

### <span data-ttu-id="181fa-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="181fa-134">-ObjectId</span></span>
<span data-ttu-id="181fa-135">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="181fa-135">Object id of the user.</span></span>

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

### <span data-ttu-id="181fa-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="181fa-136">-Skip</span></span>
<span data-ttu-id="181fa-137">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="181fa-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="181fa-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="181fa-138">-StartsWith</span></span>
<span data-ttu-id="181fa-139">Usado para localizar usuários que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="181fa-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="181fa-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="181fa-140">-UserPrincipalName</span></span>
<span data-ttu-id="181fa-141">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="181fa-141">UPN of the user.</span></span>

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

### <span data-ttu-id="181fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181fa-142">CommonParameters</span></span>
<span data-ttu-id="181fa-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181fa-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181fa-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181fa-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="181fa-145">INPUTS</span></span>

### <span data-ttu-id="181fa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="181fa-146">System.String</span></span>

### <span data-ttu-id="181fa-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="181fa-147">System.Guid</span></span>

## <span data-ttu-id="181fa-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="181fa-148">OUTPUTS</span></span>

### <span data-ttu-id="181fa-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="181fa-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="181fa-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="181fa-150">NOTES</span></span>

## <span data-ttu-id="181fa-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="181fa-151">RELATED LINKS</span></span>

[<span data-ttu-id="181fa-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="181fa-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="181fa-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="181fa-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="181fa-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="181fa-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
