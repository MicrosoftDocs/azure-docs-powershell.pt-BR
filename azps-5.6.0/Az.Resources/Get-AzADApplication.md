---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 759977fb861f0ff2f1ede1fb28af50448b5ba5ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889409"
---
# <span data-ttu-id="a57cf-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a57cf-101">Get-AzADApplication</span></span>

## <span data-ttu-id="a57cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a57cf-103">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a57cf-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="a57cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a57cf-104">SYNTAX</span></span>

### <span data-ttu-id="a57cf-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a57cf-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a57cf-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57cf-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a57cf-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57cf-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a57cf-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57cf-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a57cf-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57cf-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a57cf-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57cf-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a57cf-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a57cf-111">DESCRIPTION</span></span>
<span data-ttu-id="a57cf-112">Lista os aplicativos existentes do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a57cf-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="a57cf-113">A procurar aplicativo pode ser feita por ObjectId, ApplicationId, IdentifierUri ou DisplayName.</span><span class="sxs-lookup"><span data-stu-id="a57cf-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="a57cf-114">Se nenhum parâmetro for fornecido, ele buscará todos os aplicativos sob o locatário.</span><span class="sxs-lookup"><span data-stu-id="a57cf-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="a57cf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a57cf-115">EXAMPLES</span></span>

### <span data-ttu-id="a57cf-116">Exemplo 1 - Listar todos os aplicativos</span><span class="sxs-lookup"><span data-stu-id="a57cf-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="a57cf-117">Lista todos os aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="a57cf-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="a57cf-118">Exemplo 2 - Listar aplicativos usando paging</span><span class="sxs-lookup"><span data-stu-id="a57cf-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="a57cf-119">Lista os primeiros 100 aplicativos em um locatário.</span><span class="sxs-lookup"><span data-stu-id="a57cf-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="a57cf-120">Exemplo 3 - Obter aplicativo por URI de identificador</span><span class="sxs-lookup"><span data-stu-id="a57cf-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="a57cf-121">Obtém o aplicativo com uri identificador como " http://mySecretApp1 ".</span><span class="sxs-lookup"><span data-stu-id="a57cf-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="a57cf-122">Exemplo 4 - Obter o aplicativo por id do objeto</span><span class="sxs-lookup"><span data-stu-id="a57cf-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="a57cf-123">Obtém o aplicativo com a id do objeto '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span><span class="sxs-lookup"><span data-stu-id="a57cf-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="a57cf-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a57cf-124">PARAMETERS</span></span>

### <span data-ttu-id="a57cf-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a57cf-125">-ApplicationId</span></span>
<span data-ttu-id="a57cf-126">A ID do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="a57cf-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="a57cf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57cf-127">-DefaultProfile</span></span>
<span data-ttu-id="a57cf-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a57cf-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a57cf-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a57cf-129">-DisplayName</span></span>
<span data-ttu-id="a57cf-130">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a57cf-130">The display name of the application.</span></span>

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

### <span data-ttu-id="a57cf-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="a57cf-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="a57cf-132">Buscar todos os aplicativos começando com o nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="a57cf-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="a57cf-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="a57cf-133">-IdentifierUri</span></span>
<span data-ttu-id="a57cf-134">Identificador exclusivo Uri do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="a57cf-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="a57cf-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a57cf-135">-ObjectId</span></span>
<span data-ttu-id="a57cf-136">A id do objeto do aplicativo a ser buscado.</span><span class="sxs-lookup"><span data-stu-id="a57cf-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="a57cf-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a57cf-137">-IncludeTotalCount</span></span>
<span data-ttu-id="a57cf-138">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="a57cf-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a57cf-139">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="a57cf-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a57cf-140">-Skip</span><span class="sxs-lookup"><span data-stu-id="a57cf-140">-Skip</span></span>
<span data-ttu-id="a57cf-141">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="a57cf-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a57cf-142">-First</span><span class="sxs-lookup"><span data-stu-id="a57cf-142">-First</span></span>
<span data-ttu-id="a57cf-143">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="a57cf-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a57cf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57cf-144">CommonParameters</span></span>
<span data-ttu-id="a57cf-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57cf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57cf-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a57cf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57cf-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a57cf-147">INPUTS</span></span>

### <span data-ttu-id="a57cf-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a57cf-148">System.String</span></span>

### <span data-ttu-id="a57cf-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a57cf-149">System.Guid</span></span>

## <span data-ttu-id="a57cf-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a57cf-150">OUTPUTS</span></span>

### <span data-ttu-id="a57cf-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a57cf-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a57cf-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="a57cf-152">NOTES</span></span>

## <span data-ttu-id="a57cf-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a57cf-153">RELATED LINKS</span></span>

[<span data-ttu-id="a57cf-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a57cf-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="a57cf-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a57cf-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a57cf-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a57cf-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="a57cf-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a57cf-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a57cf-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a57cf-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a57cf-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a57cf-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

