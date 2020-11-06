---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602585"
---
# <span data-ttu-id="6d234-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d234-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="6d234-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d234-102">SYNOPSIS</span></span>
<span data-ttu-id="6d234-103">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d234-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d234-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d234-104">SYNTAX</span></span>

### <span data-ttu-id="6d234-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6d234-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6d234-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d234-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6d234-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d234-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6d234-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d234-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6d234-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d234-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6d234-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d234-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="6d234-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d234-111">DESCRIPTION</span></span>
<span data-ttu-id="6d234-112">Filtra usuários do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6d234-112">Filters active directory users.</span></span>

## <span data-ttu-id="6d234-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d234-113">EXAMPLES</span></span>

### <span data-ttu-id="6d234-114">Exemplo 1-listar todos os usuários</span><span class="sxs-lookup"><span data-stu-id="6d234-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="6d234-115">Lista todos os usuários do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="6d234-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="6d234-116">Exemplo 2-listar todos os usuários que usam paginação</span><span class="sxs-lookup"><span data-stu-id="6d234-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="6d234-117">Lista os primeiros usuários do 100 AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="6d234-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="6d234-118">Exemplo 3-obter usuário do AD por nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="6d234-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="6d234-119">Obtém o usuário do anúncio com o nome principal do usuário " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="6d234-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="6d234-120">Exemplo de 4-lista por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="6d234-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="6d234-121">Lista todos os usuários do AD cujo nome de exibição começa com "Joe".</span><span class="sxs-lookup"><span data-stu-id="6d234-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="6d234-122">OS</span><span class="sxs-lookup"><span data-stu-id="6d234-122">PARAMETERS</span></span>

### <span data-ttu-id="6d234-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d234-123">-DefaultProfile</span></span>
<span data-ttu-id="6d234-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6d234-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d234-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d234-125">-DisplayName</span></span>
<span data-ttu-id="6d234-126">O nome de exibição do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d234-126">The display name of the user.</span></span>

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

### <span data-ttu-id="6d234-127">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="6d234-127">-First</span></span>
<span data-ttu-id="6d234-128">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="6d234-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="6d234-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6d234-129">-IncludeTotalCount</span></span>
<span data-ttu-id="6d234-130">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="6d234-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="6d234-131">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="6d234-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="6d234-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="6d234-132">-Mail</span></span>
<span data-ttu-id="6d234-133">O email do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d234-133">The user mail.</span></span>

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

### <span data-ttu-id="6d234-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6d234-134">-ObjectId</span></span>
<span data-ttu-id="6d234-135">ID do objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d234-135">Object id of the user.</span></span>

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

### <span data-ttu-id="6d234-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="6d234-136">-Skip</span></span>
<span data-ttu-id="6d234-137">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="6d234-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6d234-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="6d234-138">-StartsWith</span></span>
<span data-ttu-id="6d234-139">Usado para localizar usuários que começam com a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="6d234-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="6d234-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6d234-140">-UserPrincipalName</span></span>
<span data-ttu-id="6d234-141">UPN do usuário.</span><span class="sxs-lookup"><span data-stu-id="6d234-141">UPN of the user.</span></span>

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

### <span data-ttu-id="6d234-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d234-142">CommonParameters</span></span>
<span data-ttu-id="6d234-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d234-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d234-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d234-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d234-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d234-145">INPUTS</span></span>

### <span data-ttu-id="6d234-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6d234-146">System.String</span></span>

### <span data-ttu-id="6d234-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6d234-147">System.Guid</span></span>

## <span data-ttu-id="6d234-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d234-148">OUTPUTS</span></span>

### <span data-ttu-id="6d234-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="6d234-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6d234-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d234-150">NOTES</span></span>

## <span data-ttu-id="6d234-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d234-151">RELATED LINKS</span></span>

[<span data-ttu-id="6d234-152">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d234-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="6d234-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d234-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="6d234-154">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="6d234-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

