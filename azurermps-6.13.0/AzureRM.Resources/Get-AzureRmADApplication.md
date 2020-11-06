---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: d36bca60f722498beaa831c2a630b23d8a709019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430062"
---
# <span data-ttu-id="660f2-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="660f2-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="660f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="660f2-102">SYNOPSIS</span></span>
<span data-ttu-id="660f2-103">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="660f2-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="660f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="660f2-104">SYNTAX</span></span>

### <span data-ttu-id="660f2-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="660f2-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="660f2-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f2-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="660f2-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f2-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="660f2-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f2-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="660f2-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f2-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="660f2-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f2-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="660f2-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="660f2-111">DESCRIPTION</span></span>
<span data-ttu-id="660f2-112">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="660f2-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="660f2-113">A pesquisa do aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.</span><span class="sxs-lookup"><span data-stu-id="660f2-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="660f2-114">Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.</span><span class="sxs-lookup"><span data-stu-id="660f2-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="660f2-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="660f2-115">EXAMPLES</span></span>

### <span data-ttu-id="660f2-116">Exemplo 1-listar todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="660f2-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="660f2-117">Lista todos os aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="660f2-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="660f2-118">Exemplo 2 aplicativos de lista usando paginação</span><span class="sxs-lookup"><span data-stu-id="660f2-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="660f2-119">Lista os primeiros aplicativos do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="660f2-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="660f2-120">Exemplo 3-obter aplicativo por URI identificador</span><span class="sxs-lookup"><span data-stu-id="660f2-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="660f2-121">Obtém o aplicativo com URI de identificador como " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="660f2-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="660f2-122">Exemplo 4-obter aplicativo por ID do objeto</span><span class="sxs-lookup"><span data-stu-id="660f2-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="660f2-123">Obtém o aplicativo com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 '.</span><span class="sxs-lookup"><span data-stu-id="660f2-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="660f2-124">OS</span><span class="sxs-lookup"><span data-stu-id="660f2-124">PARAMETERS</span></span>

### <span data-ttu-id="660f2-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="660f2-125">-ApplicationId</span></span>
<span data-ttu-id="660f2-126">A ID do aplicativo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="660f2-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="660f2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660f2-127">-DefaultProfile</span></span>
<span data-ttu-id="660f2-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="660f2-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="660f2-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="660f2-129">-DisplayName</span></span>
<span data-ttu-id="660f2-130">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="660f2-130">The display name of the application.</span></span>

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

### <span data-ttu-id="660f2-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="660f2-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="660f2-132">Busque todos os aplicativos que começam com o nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="660f2-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="660f2-133">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="660f2-133">-First</span></span>
<span data-ttu-id="660f2-134">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="660f2-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="660f2-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="660f2-135">-IdentifierUri</span></span>
<span data-ttu-id="660f2-136">URI do identificador exclusivo do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="660f2-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="660f2-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="660f2-137">-IncludeTotalCount</span></span>
<span data-ttu-id="660f2-138">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="660f2-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="660f2-139">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="660f2-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="660f2-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="660f2-140">-ObjectId</span></span>
<span data-ttu-id="660f2-141">A ID do objeto do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="660f2-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="660f2-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="660f2-142">-Skip</span></span>
<span data-ttu-id="660f2-143">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="660f2-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="660f2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660f2-144">CommonParameters</span></span>
<span data-ttu-id="660f2-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660f2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660f2-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660f2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660f2-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="660f2-147">INPUTS</span></span>

### <span data-ttu-id="660f2-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="660f2-148">System.Guid</span></span>

### <span data-ttu-id="660f2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="660f2-149">System.String</span></span>

## <span data-ttu-id="660f2-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="660f2-150">OUTPUTS</span></span>

### <span data-ttu-id="660f2-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="660f2-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="660f2-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="660f2-152">NOTES</span></span>

## <span data-ttu-id="660f2-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="660f2-153">RELATED LINKS</span></span>

[<span data-ttu-id="660f2-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="660f2-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="660f2-155">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="660f2-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="660f2-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="660f2-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="660f2-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="660f2-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="660f2-158">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="660f2-158">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="660f2-159">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="660f2-159">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)
