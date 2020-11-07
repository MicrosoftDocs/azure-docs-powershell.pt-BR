---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: afcb95eca70c005023bacc2b2d71d9fda54c9259
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942031"
---
# <span data-ttu-id="11b94-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="11b94-101">Get-AzADApplication</span></span>

## <span data-ttu-id="11b94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11b94-102">SYNOPSIS</span></span>
<span data-ttu-id="11b94-103">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="11b94-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="11b94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11b94-104">SYNTAX</span></span>

### <span data-ttu-id="11b94-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="11b94-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="11b94-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b94-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="11b94-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b94-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="11b94-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b94-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="11b94-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b94-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="11b94-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b94-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="11b94-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11b94-111">DESCRIPTION</span></span>
<span data-ttu-id="11b94-112">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="11b94-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="11b94-113">A pesquisa do aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.</span><span class="sxs-lookup"><span data-stu-id="11b94-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="11b94-114">Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.</span><span class="sxs-lookup"><span data-stu-id="11b94-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="11b94-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11b94-115">EXAMPLES</span></span>

### <span data-ttu-id="11b94-116">Exemplo 1-listar todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="11b94-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="11b94-117">Lista todos os aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="11b94-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="11b94-118">Exemplo 2 aplicativos de lista usando paginação</span><span class="sxs-lookup"><span data-stu-id="11b94-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="11b94-119">Lista os primeiros aplicativos do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="11b94-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="11b94-120">Exemplo 3-obter aplicativo por URI identificador</span><span class="sxs-lookup"><span data-stu-id="11b94-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="11b94-121">Obtém o aplicativo com URI de identificador como " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="11b94-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="11b94-122">Exemplo 4-obter aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="11b94-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="11b94-123">Obtém o aplicativo com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 '.</span><span class="sxs-lookup"><span data-stu-id="11b94-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="11b94-124">OS</span><span class="sxs-lookup"><span data-stu-id="11b94-124">PARAMETERS</span></span>

### <span data-ttu-id="11b94-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11b94-125">-ApplicationId</span></span>
<span data-ttu-id="11b94-126">A ID do aplicativo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="11b94-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b94-127">-DefaultProfile</span></span>
<span data-ttu-id="11b94-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="11b94-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11b94-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11b94-129">-DisplayName</span></span>
<span data-ttu-id="11b94-130">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11b94-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="11b94-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="11b94-132">Busque todos os aplicativos que começam com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="11b94-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="11b94-133">-IdentifierUri</span></span>
<span data-ttu-id="11b94-134">URI do identificador exclusivo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="11b94-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="11b94-135">-ObjectId</span></span>
<span data-ttu-id="11b94-136">A ID do objeto do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="11b94-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b94-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="11b94-137">-IncludeTotalCount</span></span>
<span data-ttu-id="11b94-138">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="11b94-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="11b94-139">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="11b94-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="11b94-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="11b94-140">-Skip</span></span>
<span data-ttu-id="11b94-141">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="11b94-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="11b94-142">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="11b94-142">-First</span></span>
<span data-ttu-id="11b94-143">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="11b94-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="11b94-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b94-144">CommonParameters</span></span>
<span data-ttu-id="11b94-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b94-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b94-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11b94-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b94-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11b94-147">INPUTS</span></span>

### <span data-ttu-id="11b94-148">System. String</span><span class="sxs-lookup"><span data-stu-id="11b94-148">System.String</span></span>

### <span data-ttu-id="11b94-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="11b94-149">System.Guid</span></span>

## <span data-ttu-id="11b94-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11b94-150">OUTPUTS</span></span>

### <span data-ttu-id="11b94-151">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="11b94-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="11b94-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11b94-152">NOTES</span></span>

## <span data-ttu-id="11b94-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11b94-153">RELATED LINKS</span></span>

[<span data-ttu-id="11b94-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="11b94-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="11b94-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="11b94-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="11b94-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="11b94-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="11b94-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="11b94-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="11b94-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="11b94-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

