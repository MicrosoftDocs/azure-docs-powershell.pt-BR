---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427357"
---
# <span data-ttu-id="2468c-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2468c-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="2468c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2468c-102">SYNOPSIS</span></span>
<span data-ttu-id="2468c-103">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2468c-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="2468c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2468c-104">SYNTAX</span></span>

### <span data-ttu-id="2468c-105">EmptyParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2468c-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2468c-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2468c-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="2468c-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2468c-112">DESCRIPTION</span></span>
<span data-ttu-id="2468c-113">Filtra as entidades de serviço do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2468c-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="2468c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2468c-114">EXAMPLES</span></span>

### <span data-ttu-id="2468c-115">Exemplo 1: listar entidades de serviço de anúncios</span><span class="sxs-lookup"><span data-stu-id="2468c-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="2468c-116">Lista todas as entidades de serviço de anúncio em um locatário.</span><span class="sxs-lookup"><span data-stu-id="2468c-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="2468c-117">Exemplo 2: listar entidades de serviço de anúncios usando paginação</span><span class="sxs-lookup"><span data-stu-id="2468c-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="2468c-118">Lista as primeiras entidades de serviço do anúncio do 100 em um locatário.</span><span class="sxs-lookup"><span data-stu-id="2468c-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="2468c-119">Exemplo 3: listar entidades de serviço por SPN</span><span class="sxs-lookup"><span data-stu-id="2468c-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="2468c-120">Lista as entidades de serviço com o SPN ' 36f81fc3-b00f-48CD-8218-3879f51ff39f '.</span><span class="sxs-lookup"><span data-stu-id="2468c-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="2468c-121">Exemplo 4: listar as entidades de serviço por cadeia de pesquisa</span><span class="sxs-lookup"><span data-stu-id="2468c-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="2468c-122">Lista todas as entidades de serviço de anúncio cujo nome para exibição comece com "Web".</span><span class="sxs-lookup"><span data-stu-id="2468c-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="2468c-123">Exemplo 5: listar as entidades de serviço por tubulação</span><span class="sxs-lookup"><span data-stu-id="2468c-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="2468c-124">Obtém o aplicativo do anúncio com a ID de objeto ' 39e64ec6-569B-4030-8e1c-c3c519a05d69 ' e a canaliza para o cmdlet Get-AzADServicePrincipal para listar todas as entidades de serviço desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2468c-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="2468c-125">OS</span><span class="sxs-lookup"><span data-stu-id="2468c-125">PARAMETERS</span></span>

### <span data-ttu-id="2468c-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2468c-126">-ApplicationId</span></span>
<span data-ttu-id="2468c-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="2468c-127">The service principal application id.</span></span>

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

### <span data-ttu-id="2468c-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2468c-128">-ApplicationObject</span></span>
<span data-ttu-id="2468c-129">O objeto de aplicativo cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="2468c-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="2468c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2468c-130">-DefaultProfile</span></span>
<span data-ttu-id="2468c-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2468c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2468c-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2468c-132">-DisplayName</span></span>
<span data-ttu-id="2468c-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2468c-133">The service principal display name.</span></span>

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

### <span data-ttu-id="2468c-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="2468c-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="2468c-135">A cadeia de caracteres de pesquisa principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="2468c-135">The service principal search string.</span></span>

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

### <span data-ttu-id="2468c-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2468c-136">-ObjectId</span></span>
<span data-ttu-id="2468c-137">ID de objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="2468c-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="2468c-138">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="2468c-138">-ServicePrincipalName</span></span>
<span data-ttu-id="2468c-139">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="2468c-139">SPN of the service.</span></span>

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

### <span data-ttu-id="2468c-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2468c-140">-IncludeTotalCount</span></span>
<span data-ttu-id="2468c-141">Informa o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="2468c-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="2468c-142">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="2468c-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="2468c-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="2468c-143">-Skip</span></span>
<span data-ttu-id="2468c-144">Ignora os primeiros N objetos e, em seguida, obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="2468c-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="2468c-145">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="2468c-145">-First</span></span>
<span data-ttu-id="2468c-146">O número máximo de objetos a serem retornados.</span><span class="sxs-lookup"><span data-stu-id="2468c-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="2468c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2468c-147">CommonParameters</span></span>
<span data-ttu-id="2468c-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2468c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2468c-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2468c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2468c-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2468c-150">INPUTS</span></span>

### <span data-ttu-id="2468c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="2468c-151">System.String</span></span>

### <span data-ttu-id="2468c-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2468c-152">System.Guid</span></span>

### <span data-ttu-id="2468c-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2468c-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="2468c-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2468c-154">OUTPUTS</span></span>

### <span data-ttu-id="2468c-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2468c-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2468c-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2468c-156">NOTES</span></span>

## <span data-ttu-id="2468c-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2468c-157">RELATED LINKS</span></span>

[<span data-ttu-id="2468c-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2468c-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="2468c-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2468c-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="2468c-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2468c-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="2468c-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2468c-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="2468c-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2468c-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

