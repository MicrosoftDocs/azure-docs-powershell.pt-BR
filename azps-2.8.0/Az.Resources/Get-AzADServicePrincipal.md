---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772606"
---
# <span data-ttu-id="f06db-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f06db-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="f06db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f06db-102">SYNOPSIS</span></span>
<span data-ttu-id="f06db-103">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f06db-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="f06db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f06db-104">SYNTAX</span></span>

### <span data-ttu-id="f06db-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f06db-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f06db-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="f06db-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f06db-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f06db-112">DESCRIPTION</span></span>
<span data-ttu-id="f06db-113">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f06db-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="f06db-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f06db-114">EXAMPLES</span></span>

### <span data-ttu-id="f06db-115">Exemplo 1-lista de entidades de serviço de anúncios</span><span class="sxs-lookup"><span data-stu-id="f06db-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="f06db-116">Lista todas as entidades de serviço de anúncio em um locatário.</span><span class="sxs-lookup"><span data-stu-id="f06db-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="f06db-117">Exemplo 2-lista de entidades de serviço de anúncios usando paginação</span><span class="sxs-lookup"><span data-stu-id="f06db-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="f06db-118">Lista as primeiras entidades de serviço do anúncio do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="f06db-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="f06db-119">Exemplo de entidades de serviço de 3 listas por SPN</span><span class="sxs-lookup"><span data-stu-id="f06db-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="f06db-120">Lista as entidades de serviço com o SPN ' 36f81fc3-b00f-48CD-8218-3879f51ff39f '.</span><span class="sxs-lookup"><span data-stu-id="f06db-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="f06db-121">Exemplo de entidades de serviço de 4 listas por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="f06db-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="f06db-122">Lista todas as entidades de serviço de anúncio cujo nome para exibição comece com "Web".</span><span class="sxs-lookup"><span data-stu-id="f06db-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="f06db-123">Exemplo de entidades de serviço de 5 listas por tubulação</span><span class="sxs-lookup"><span data-stu-id="f06db-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="f06db-124">Obtém o aplicativo do anúncio com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 ' e a canaliza para o cmdlet Get-AzADServicePrincipal para listar todas as entidades de serviço desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f06db-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="f06db-125">OS</span><span class="sxs-lookup"><span data-stu-id="f06db-125">PARAMETERS</span></span>

### <span data-ttu-id="f06db-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f06db-126">-ApplicationId</span></span>
<span data-ttu-id="f06db-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="f06db-127">The service principal application id.</span></span>

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

### <span data-ttu-id="f06db-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="f06db-128">-ApplicationObject</span></span>
<span data-ttu-id="f06db-129">O objeto de aplicativo cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="f06db-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f06db-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06db-130">-DefaultProfile</span></span>
<span data-ttu-id="f06db-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f06db-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f06db-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f06db-132">-DisplayName</span></span>
<span data-ttu-id="f06db-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f06db-133">The service principal display name.</span></span>

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

### <span data-ttu-id="f06db-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="f06db-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="f06db-135">A cadeia de caracteres de pesquisa principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="f06db-135">The service principal search string.</span></span>

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

### <span data-ttu-id="f06db-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f06db-136">-ObjectId</span></span>
<span data-ttu-id="f06db-137">ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="f06db-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="f06db-138">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="f06db-138">-ServicePrincipalName</span></span>
<span data-ttu-id="f06db-139">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="f06db-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06db-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f06db-140">-IncludeTotalCount</span></span>
<span data-ttu-id="f06db-141">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="f06db-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f06db-142">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="f06db-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f06db-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="f06db-143">-Skip</span></span>
<span data-ttu-id="f06db-144">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="f06db-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f06db-145">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="f06db-145">-First</span></span>
<span data-ttu-id="f06db-146">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="f06db-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f06db-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06db-147">CommonParameters</span></span>
<span data-ttu-id="f06db-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06db-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06db-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f06db-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06db-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f06db-150">INPUTS</span></span>

### <span data-ttu-id="f06db-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f06db-151">System.String</span></span>

### <span data-ttu-id="f06db-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f06db-152">System.Guid</span></span>

### <span data-ttu-id="f06db-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f06db-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f06db-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f06db-154">OUTPUTS</span></span>

### <span data-ttu-id="f06db-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f06db-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f06db-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f06db-156">NOTES</span></span>

## <span data-ttu-id="f06db-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f06db-157">RELATED LINKS</span></span>

[<span data-ttu-id="f06db-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f06db-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="f06db-159">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f06db-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="f06db-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f06db-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="f06db-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f06db-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="f06db-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f06db-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

