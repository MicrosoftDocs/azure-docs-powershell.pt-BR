---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: ecb5b1200bacab12f7715600b7fcf60b78b81092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887154"
---
# <span data-ttu-id="756cb-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="756cb-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="756cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756cb-102">SYNOPSIS</span></span>
<span data-ttu-id="756cb-103">Crie ou atualize um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="756cb-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="756cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="756cb-104">SYNTAX</span></span>

### <span data-ttu-id="756cb-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="756cb-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="756cb-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="756cb-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="756cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="756cb-107">DESCRIPTION</span></span>
<span data-ttu-id="756cb-108">Crie ou atualize um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="756cb-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="756cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="756cb-109">EXAMPLES</span></span>

### <span data-ttu-id="756cb-110">Exemplo 1: cria novo pacote MSIX no HostPool por meio do alias do pacote</span><span class="sxs-lookup"><span data-stu-id="756cb-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="756cb-111">Este comando adiciona o pacote MSIX do caminho de imagem especificado ao HostPool</span><span class="sxs-lookup"><span data-stu-id="756cb-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="756cb-112">Exemplo 2: cria novo pacote MSIX no HostPool</span><span class="sxs-lookup"><span data-stu-id="756cb-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="756cb-113">Este comando adiciona Pacote MSIX no HostPool especificado</span><span class="sxs-lookup"><span data-stu-id="756cb-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="756cb-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="756cb-114">PARAMETERS</span></span>

### <span data-ttu-id="756cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756cb-115">-DefaultProfile</span></span>
<span data-ttu-id="756cb-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="756cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="756cb-117">-DisplayName</span></span>
<span data-ttu-id="756cb-118">Nome amigável a ser exibido no portal.</span><span class="sxs-lookup"><span data-stu-id="756cb-118">User friendly Name to be displayed in the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="756cb-119">-FullName</span></span>
<span data-ttu-id="756cb-120">O nome completo do pacote específico da versão do pacote MSIX no hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="756cb-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="756cb-121">-HostPoolName</span></span>
<span data-ttu-id="756cb-122">O nome do pool de host no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="756cb-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="756cb-123">-ImagePath</span></span>
<span data-ttu-id="756cb-124">Caminho de imagem VHD/CIM no Compartilhamento de Rede.</span><span class="sxs-lookup"><span data-stu-id="756cb-124">VHD/CIM image path on Network Share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="756cb-125">-IsActive</span></span>
<span data-ttu-id="756cb-126">Tornar essa versão do pacote a ativa em todo o hostpool.</span><span class="sxs-lookup"><span data-stu-id="756cb-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="756cb-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="756cb-127">-IsRegularRegistration</span></span>
<span data-ttu-id="756cb-128">Especifica como registrar o pacote no feed.</span><span class="sxs-lookup"><span data-stu-id="756cb-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="756cb-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="756cb-129">-LastUpdated</span></span>
<span data-ttu-id="756cb-130">Pacote data foi atualizado pela última vez, encontrado no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="756cb-131">-PackageAlias</span></span>
<span data-ttu-id="756cb-132">Alias do pacote da extração de imagem MSIX</span><span class="sxs-lookup"><span data-stu-id="756cb-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="756cb-133">-PackageApplication</span></span>
<span data-ttu-id="756cb-134">Lista de aplicativos de pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-134">List of package applications.</span></span>

<span data-ttu-id="756cb-135">Para construir, consulte a seção NOTES para propriedades PACKAGEAPPLICATION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="756cb-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="756cb-136">-PackageDependency</span></span>
<span data-ttu-id="756cb-137">Lista de dependências de pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-137">List of package dependencies.</span></span>

<span data-ttu-id="756cb-138">Para construir, consulte a seção NOTES para propriedades PACKAGEDEPENDENCY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="756cb-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="756cb-139">-PackageFamilyName</span></span>
<span data-ttu-id="756cb-140">Nome da família do pacote appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="756cb-141">Contém Nome do Pacote e Nome do Editor.</span><span class="sxs-lookup"><span data-stu-id="756cb-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="756cb-142">-PackageName</span></span>
<span data-ttu-id="756cb-143">Nome do pacote appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="756cb-144">-PackageRelativePath</span></span>
<span data-ttu-id="756cb-145">Caminho Relativo para o pacote dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="756cb-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756cb-146">-ResourceGroupName</span></span>
<span data-ttu-id="756cb-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="756cb-147">The name of the resource group.</span></span>
<span data-ttu-id="756cb-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="756cb-148">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="756cb-149">-SubscriptionId</span></span>
<span data-ttu-id="756cb-150">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="756cb-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-151">-Version</span><span class="sxs-lookup"><span data-stu-id="756cb-151">-Version</span></span>
<span data-ttu-id="756cb-152">Versão do pacote encontrada na appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="756cb-153">-Confirm</span></span>
<span data-ttu-id="756cb-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="756cb-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756cb-155">-WhatIf</span></span>
<span data-ttu-id="756cb-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="756cb-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="756cb-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="756cb-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756cb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756cb-158">CommonParameters</span></span>
<span data-ttu-id="756cb-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="756cb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756cb-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="756cb-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756cb-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="756cb-161">INPUTS</span></span>

## <span data-ttu-id="756cb-162">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="756cb-162">OUTPUTS</span></span>

### <span data-ttu-id="756cb-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="756cb-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="756cb-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="756cb-164">NOTES</span></span>

<span data-ttu-id="756cb-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="756cb-165">ALIASES</span></span>

<span data-ttu-id="756cb-166">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="756cb-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="756cb-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="756cb-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="756cb-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="756cb-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="756cb-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: Lista de aplicativos de pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="756cb-170">`[AppId <String>]`: ID do aplicativo de pacote, encontrada appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="756cb-171">`[AppUserModelId <String>]`: Usado para ativar o Aplicativo de Pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="756cb-172">Consiste em Nome do Pacote e ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="756cb-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="756cb-173">Encontrado em appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="756cb-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="756cb-174">`[Description <String>]`: Descrição do Aplicativo de Pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="756cb-175">`[FriendlyName <String>]`: Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="756cb-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="756cb-176">`[IconImageName <String>]`: Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="756cb-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="756cb-177">`[RawIcon <Byte[]>]`: o ícone de uma cadeia de caracteres de 64 bits como uma matriz de byte.</span><span class="sxs-lookup"><span data-stu-id="756cb-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="756cb-178">`[RawPng <Byte[]>]`: o ícone de uma cadeia de caracteres de 64 bits como uma matriz de byte.</span><span class="sxs-lookup"><span data-stu-id="756cb-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="756cb-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: Lista de dependências de pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="756cb-180">`[DependencyName <String>]`: Nome da dependência do pacote.</span><span class="sxs-lookup"><span data-stu-id="756cb-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="756cb-181">`[MinVersion <String>]`: A versão de dependência necessária.</span><span class="sxs-lookup"><span data-stu-id="756cb-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="756cb-182">`[Publisher <String>]`: Nome do editor de dependência.</span><span class="sxs-lookup"><span data-stu-id="756cb-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="756cb-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="756cb-183">RELATED LINKS</span></span>

