---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 659c2a026099eaa8764030b86a40d9ca6d4d2333
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886599"
---
# <span data-ttu-id="6fbf7-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fbf7-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="6fbf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbf7-103">Filtra as entidades de serviço do active directory.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="6fbf7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6fbf7-104">SYNTAX</span></span>

### <span data-ttu-id="6fbf7-105">EmptyParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6fbf7-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="6fbf7-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbf7-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="6fbf7-112">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6fbf7-112">DESCRIPTION</span></span>
<span data-ttu-id="6fbf7-113">Filtra as entidades de serviço do active directory.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="6fbf7-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-114">EXAMPLES</span></span>

### <span data-ttu-id="6fbf7-115">Exemplo 1: Listar entidades de serviço do AD</span><span class="sxs-lookup"><span data-stu-id="6fbf7-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="6fbf7-116">Lista todas as entidades de serviço do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="6fbf7-117">Exemplo 2: listar entidades de serviço do AD usando paging</span><span class="sxs-lookup"><span data-stu-id="6fbf7-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="6fbf7-118">Lista os primeiros 100 entidades de serviço do AD em um locatário.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="6fbf7-119">Exemplo 3: Listar entidades de serviço pelo SPN</span><span class="sxs-lookup"><span data-stu-id="6fbf7-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="6fbf7-120">Lista entidades de serviço com o SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="6fbf7-121">Exemplo 4: Listar entidades de serviço por cadeia de caracteres de pesquisa</span><span class="sxs-lookup"><span data-stu-id="6fbf7-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="6fbf7-122">Lista todas as entidades de serviço do AD cujo nome de exibição começa com "Web".</span><span class="sxs-lookup"><span data-stu-id="6fbf7-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="6fbf7-123">Exemplo 5: Listar entidades de serviço por canalização</span><span class="sxs-lookup"><span data-stu-id="6fbf7-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="6fbf7-124">Obtém o aplicativo AD com a id do objeto '39e64ec6-569b-4030-8e1c-c3c519a05d69' e o canalizará para o cmdlet Get-AzADServicePrincipal para listar todas as entidades de serviço desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="6fbf7-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-125">PARAMETERS</span></span>

### <span data-ttu-id="6fbf7-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6fbf7-126">-ApplicationId</span></span>
<span data-ttu-id="6fbf7-127">A ID do aplicativo principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-127">The service principal application id.</span></span>

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

### <span data-ttu-id="6fbf7-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="6fbf7-128">-ApplicationObject</span></span>
<span data-ttu-id="6fbf7-129">O objeto application cuja entidade de serviço está sendo recuperada.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="6fbf7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbf7-130">-DefaultProfile</span></span>
<span data-ttu-id="6fbf7-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6fbf7-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fbf7-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6fbf7-132">-DisplayName</span></span>
<span data-ttu-id="6fbf7-133">O nome de exibição da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-133">The service principal display name.</span></span>

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

### <span data-ttu-id="6fbf7-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6fbf7-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="6fbf7-135">A cadeia de caracteres de pesquisa da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-135">The service principal search string.</span></span>

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

### <span data-ttu-id="6fbf7-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6fbf7-136">-ObjectId</span></span>
<span data-ttu-id="6fbf7-137">ID do objeto da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="6fbf7-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="6fbf7-138">-ServicePrincipalName</span></span>
<span data-ttu-id="6fbf7-139">SPN do serviço.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-139">SPN of the service.</span></span>

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

### <span data-ttu-id="6fbf7-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="6fbf7-140">-IncludeTotalCount</span></span>
<span data-ttu-id="6fbf7-141">Relata o número de objetos no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="6fbf7-142">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="6fbf7-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="6fbf7-143">-Skip</span></span>
<span data-ttu-id="6fbf7-144">Ignora os primeiros objetos N e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="6fbf7-145">-First</span><span class="sxs-lookup"><span data-stu-id="6fbf7-145">-First</span></span>
<span data-ttu-id="6fbf7-146">O número máximo de objetos a retornar.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="6fbf7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbf7-147">CommonParameters</span></span>
<span data-ttu-id="6fbf7-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbf7-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fbf7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbf7-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-150">INPUTS</span></span>

### <span data-ttu-id="6fbf7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6fbf7-151">System.String</span></span>

### <span data-ttu-id="6fbf7-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6fbf7-152">System.Guid</span></span>

### <span data-ttu-id="6fbf7-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6fbf7-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6fbf7-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-154">OUTPUTS</span></span>

### <span data-ttu-id="6fbf7-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fbf7-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="6fbf7-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="6fbf7-156">NOTES</span></span>

## <span data-ttu-id="6fbf7-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fbf7-157">RELATED LINKS</span></span>

[<span data-ttu-id="6fbf7-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fbf7-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="6fbf7-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fbf7-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="6fbf7-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6fbf7-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="6fbf7-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6fbf7-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="6fbf7-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6fbf7-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

