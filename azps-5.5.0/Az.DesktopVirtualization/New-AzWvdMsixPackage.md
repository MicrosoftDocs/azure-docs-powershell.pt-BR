---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: 162071e07e8081f80e4187f049aef8931dcffc78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115826"
---
# <span data-ttu-id="a65b2-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a65b2-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="a65b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a65b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a65b2-103">Criar ou atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="a65b2-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="a65b2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65b2-104">SYNTAX</span></span>

### <span data-ttu-id="a65b2-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="a65b2-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a65b2-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="a65b2-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a65b2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a65b2-108">Criar ou atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="a65b2-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="a65b2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a65b2-109">EXAMPLES</span></span>

### <span data-ttu-id="a65b2-110">Exemplo 1: cria um novo pacote MSIX no HostPool via Alias de Pacote</span><span class="sxs-lookup"><span data-stu-id="a65b2-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="a65b2-111">Este comando adiciona o pacote MSIX do caminho de imagem especificado ao HostPool</span><span class="sxs-lookup"><span data-stu-id="a65b2-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="a65b2-112">Exemplo 2: cria um novo pacote MSIX no HostPool</span><span class="sxs-lookup"><span data-stu-id="a65b2-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="a65b2-113">Este comando adiciona o Pacote MSIX no HostPool especificado</span><span class="sxs-lookup"><span data-stu-id="a65b2-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="a65b2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a65b2-114">PARAMETERS</span></span>

### <span data-ttu-id="a65b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65b2-115">-DefaultProfile</span></span>
<span data-ttu-id="a65b2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a65b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65b2-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a65b2-117">-DisplayName</span></span>
<span data-ttu-id="a65b2-118">Nome amigável a ser exibido no portal.</span><span class="sxs-lookup"><span data-stu-id="a65b2-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="a65b2-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="a65b2-119">-FullName</span></span>
<span data-ttu-id="a65b2-120">O nome completo do pacote de versão específico do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="a65b2-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="a65b2-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a65b2-121">-HostPoolName</span></span>
<span data-ttu-id="a65b2-122">O nome do pool de host dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a65b2-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a65b2-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="a65b2-123">-ImagePath</span></span>
<span data-ttu-id="a65b2-124">Caminho de imagem DE SOD/LTD no Compartilhamento de Rede.</span><span class="sxs-lookup"><span data-stu-id="a65b2-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="a65b2-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="a65b2-125">-IsActive</span></span>
<span data-ttu-id="a65b2-126">Faça com que esta versão do pacote seja a ativa na hostpool.</span><span class="sxs-lookup"><span data-stu-id="a65b2-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="a65b2-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="a65b2-127">-IsRegularRegistration</span></span>
<span data-ttu-id="a65b2-128">Especifica como registrar Pacote no feed.</span><span class="sxs-lookup"><span data-stu-id="a65b2-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="a65b2-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="a65b2-129">-LastUpdated</span></span>
<span data-ttu-id="a65b2-130">Pacote de Datas foi atualizado pela última vez, encontrado no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="a65b2-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="a65b2-131">-PackageAlias</span></span>
<span data-ttu-id="a65b2-132">Alias de Pacote da extração de imagem MSIX</span><span class="sxs-lookup"><span data-stu-id="a65b2-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="a65b2-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="a65b2-133">-PackageApplication</span></span>
<span data-ttu-id="a65b2-134">Lista de aplicativos de pacote.</span><span class="sxs-lookup"><span data-stu-id="a65b2-134">List of package applications.</span></span>

<span data-ttu-id="a65b2-135">Para construir, confira a seção ANOTAÇÕES para propriedades PACKAGEAPPLICATION e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a65b2-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a65b2-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="a65b2-136">-PackageDependency</span></span>
<span data-ttu-id="a65b2-137">Lista de dependências de pacotes.</span><span class="sxs-lookup"><span data-stu-id="a65b2-137">List of package dependencies.</span></span>

<span data-ttu-id="a65b2-138">Para construir, consulte a seção ANOTAÇÕES para propriedades PACKAGEDEPENDENCY e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a65b2-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

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

### <span data-ttu-id="a65b2-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="a65b2-139">-PackageFamilyName</span></span>
<span data-ttu-id="a65b2-140">Nome da família do pacote appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="a65b2-141">Contém o Nome do Pacote e o nome do Publisher.</span><span class="sxs-lookup"><span data-stu-id="a65b2-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="a65b2-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="a65b2-142">-PackageName</span></span>
<span data-ttu-id="a65b2-143">Nome do pacote do appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="a65b2-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="a65b2-144">-PackageRelativePath</span></span>
<span data-ttu-id="a65b2-145">Caminho Relativo para o pacote dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="a65b2-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="a65b2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65b2-146">-ResourceGroupName</span></span>
<span data-ttu-id="a65b2-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a65b2-147">The name of the resource group.</span></span>
<span data-ttu-id="a65b2-148">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a65b2-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a65b2-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a65b2-149">-SubscriptionId</span></span>
<span data-ttu-id="a65b2-150">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a65b2-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a65b2-151">-Versão</span><span class="sxs-lookup"><span data-stu-id="a65b2-151">-Version</span></span>
<span data-ttu-id="a65b2-152">Versão do pacote encontrada na appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="a65b2-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a65b2-153">-Confirm</span></span>
<span data-ttu-id="a65b2-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a65b2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65b2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65b2-155">-WhatIf</span></span>
<span data-ttu-id="a65b2-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a65b2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65b2-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a65b2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65b2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65b2-158">CommonParameters</span></span>
<span data-ttu-id="a65b2-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65b2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65b2-160">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a65b2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65b2-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="a65b2-161">INPUTS</span></span>

## <span data-ttu-id="a65b2-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="a65b2-162">OUTPUTS</span></span>

### <span data-ttu-id="a65b2-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="a65b2-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="a65b2-164">Notas</span><span class="sxs-lookup"><span data-stu-id="a65b2-164">NOTES</span></span>

<span data-ttu-id="a65b2-165">Aliases</span><span class="sxs-lookup"><span data-stu-id="a65b2-165">ALIASES</span></span>

<span data-ttu-id="a65b2-166">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a65b2-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a65b2-167">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a65b2-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a65b2-168">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a65b2-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a65b2-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: Lista de aplicativos de pacote.</span><span class="sxs-lookup"><span data-stu-id="a65b2-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="a65b2-170">`[AppId <String>]`: ID do Aplicativo de Pacote, encontrada no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="a65b2-171">`[AppUserModelId <String>]`: Usado para ativar o Aplicativo de Pacote.</span><span class="sxs-lookup"><span data-stu-id="a65b2-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="a65b2-172">Consiste em Nome do Pacote e ID do Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a65b2-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="a65b2-173">Encontrado no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="a65b2-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="a65b2-174">`[Description <String>]`: Descrição do Aplicativo de Pacote.</span><span class="sxs-lookup"><span data-stu-id="a65b2-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="a65b2-175">`[FriendlyName <String>]`: Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="a65b2-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="a65b2-176">`[IconImageName <String>]`: Nome amigável.</span><span class="sxs-lookup"><span data-stu-id="a65b2-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="a65b2-177">`[RawIcon <Byte[]>]`: o ícone de uma cadeia de 64 bits como uma matriz de byte.</span><span class="sxs-lookup"><span data-stu-id="a65b2-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="a65b2-178">`[RawPng <Byte[]>]`: o ícone de uma cadeia de 64 bits como uma matriz de byte.</span><span class="sxs-lookup"><span data-stu-id="a65b2-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="a65b2-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: Lista de dependências de pacotes.</span><span class="sxs-lookup"><span data-stu-id="a65b2-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="a65b2-180">`[DependencyName <String>]`: Nome da dependência do pacote.</span><span class="sxs-lookup"><span data-stu-id="a65b2-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="a65b2-181">`[MinVersion <String>]`: a versão de dependência necessária.</span><span class="sxs-lookup"><span data-stu-id="a65b2-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="a65b2-182">`[Publisher <String>]`: Nome do editor de dependência.</span><span class="sxs-lookup"><span data-stu-id="a65b2-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="a65b2-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a65b2-183">RELATED LINKS</span></span>

