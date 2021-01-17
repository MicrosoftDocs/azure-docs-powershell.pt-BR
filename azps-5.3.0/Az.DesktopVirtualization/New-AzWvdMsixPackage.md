---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: 162071e07e8081f80e4187f049aef8931dcffc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429427"
---
# <span data-ttu-id="176a7-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="176a7-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="176a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="176a7-102">SYNOPSIS</span></span>
<span data-ttu-id="176a7-103">Criar ou atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="176a7-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="176a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="176a7-104">SYNTAX</span></span>

### <span data-ttu-id="176a7-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="176a7-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="176a7-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="176a7-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="176a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="176a7-107">DESCRIPTION</span></span>
<span data-ttu-id="176a7-108">Criar ou atualizar um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="176a7-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="176a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="176a7-109">EXAMPLES</span></span>

### <span data-ttu-id="176a7-110">Exemplo 1: cria um novo pacote MSIX no HostPool via alias de pacote</span><span class="sxs-lookup"><span data-stu-id="176a7-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="176a7-111">Esse comando adiciona um pacote MSIX do caminho de imagem especificado para HostPool</span><span class="sxs-lookup"><span data-stu-id="176a7-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="176a7-112">Exemplo 2: cria um novo pacote MSIX no HostPool</span><span class="sxs-lookup"><span data-stu-id="176a7-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="176a7-113">Esse comando adiciona um pacote MSIX no HostPool especificado</span><span class="sxs-lookup"><span data-stu-id="176a7-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="176a7-114">OS</span><span class="sxs-lookup"><span data-stu-id="176a7-114">PARAMETERS</span></span>

### <span data-ttu-id="176a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176a7-115">-DefaultProfile</span></span>
<span data-ttu-id="176a7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="176a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176a7-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="176a7-117">-DisplayName</span></span>
<span data-ttu-id="176a7-118">Nome amigável do usuário a ser exibido no Portal.</span><span class="sxs-lookup"><span data-stu-id="176a7-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="176a7-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="176a7-119">-FullName</span></span>
<span data-ttu-id="176a7-120">O nome completo do pacote de versão específica do pacote MSIX dentro do hostpool especificado</span><span class="sxs-lookup"><span data-stu-id="176a7-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="176a7-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="176a7-121">-HostPoolName</span></span>
<span data-ttu-id="176a7-122">O nome do pool de hosts dentro do grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="176a7-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="176a7-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="176a7-123">-ImagePath</span></span>
<span data-ttu-id="176a7-124">Caminho da imagem VHD/CIM no compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="176a7-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="176a7-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="176a7-125">-IsActive</span></span>
<span data-ttu-id="176a7-126">Faça desta versão do pacote a que está ativa em todo o hostpool.</span><span class="sxs-lookup"><span data-stu-id="176a7-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="176a7-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="176a7-127">-IsRegularRegistration</span></span>
<span data-ttu-id="176a7-128">Especifica como registrar o pacote no feed.</span><span class="sxs-lookup"><span data-stu-id="176a7-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="176a7-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="176a7-129">-LastUpdated</span></span>
<span data-ttu-id="176a7-130">O pacote de data foi atualizado pela última vez em appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="176a7-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="176a7-131">-PackageAlias</span></span>
<span data-ttu-id="176a7-132">Alias do pacote da imagem extrair MSIX</span><span class="sxs-lookup"><span data-stu-id="176a7-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="176a7-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="176a7-133">-PackageApplication</span></span>
<span data-ttu-id="176a7-134">Lista de aplicativos do pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-134">List of package applications.</span></span>

<span data-ttu-id="176a7-135">Para construir, consulte a seção notas para propriedades PACKAGEAPPLICATION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="176a7-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="176a7-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="176a7-136">-PackageDependency</span></span>
<span data-ttu-id="176a7-137">Lista de dependências do pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-137">List of package dependencies.</span></span>

<span data-ttu-id="176a7-138">Para construir, consulte a seção notas para propriedades PACKAGEDEPENDENCY e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="176a7-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

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

### <span data-ttu-id="176a7-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="176a7-139">-PackageFamilyName</span></span>
<span data-ttu-id="176a7-140">Nome da família de pacotes em appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="176a7-141">Contém o nome do pacote e o nome do editor.</span><span class="sxs-lookup"><span data-stu-id="176a7-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="176a7-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="176a7-142">-PackageName</span></span>
<span data-ttu-id="176a7-143">Nome do pacote de appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="176a7-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="176a7-144">-PackageRelativePath</span></span>
<span data-ttu-id="176a7-145">Caminho relativo para o pacote dentro da imagem.</span><span class="sxs-lookup"><span data-stu-id="176a7-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="176a7-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176a7-146">-ResourceGroupName</span></span>
<span data-ttu-id="176a7-147">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="176a7-147">The name of the resource group.</span></span>
<span data-ttu-id="176a7-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="176a7-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="176a7-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="176a7-149">-SubscriptionId</span></span>
<span data-ttu-id="176a7-150">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="176a7-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="176a7-151">-Versão</span><span class="sxs-lookup"><span data-stu-id="176a7-151">-Version</span></span>
<span data-ttu-id="176a7-152">Versão do pacote encontrada no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="176a7-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="176a7-153">-Confirm</span></span>
<span data-ttu-id="176a7-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176a7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176a7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176a7-155">-WhatIf</span></span>
<span data-ttu-id="176a7-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="176a7-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176a7-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="176a7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176a7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176a7-158">CommonParameters</span></span>
<span data-ttu-id="176a7-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176a7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176a7-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="176a7-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176a7-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="176a7-161">INPUTS</span></span>

## <span data-ttu-id="176a7-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="176a7-162">OUTPUTS</span></span>

### <span data-ttu-id="176a7-163">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201102Preview. IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="176a7-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="176a7-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="176a7-164">NOTES</span></span>

<span data-ttu-id="176a7-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="176a7-165">ALIASES</span></span>

<span data-ttu-id="176a7-166">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="176a7-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="176a7-167">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="176a7-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="176a7-168">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="176a7-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="176a7-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >: lista de aplicativos do pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="176a7-170">`[AppId <String>]`: ID do aplicativo de pacote, encontrado em appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="176a7-171">`[AppUserModelId <String>]`: Usado para ativar o aplicativo de pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="176a7-172">Consiste no nome do pacote e ApplicationID.</span><span class="sxs-lookup"><span data-stu-id="176a7-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="176a7-173">Encontrado no appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="176a7-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="176a7-174">`[Description <String>]`: Descrição do aplicativo de pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="176a7-175">`[FriendlyName <String>]`: Nome amigável do usuário.</span><span class="sxs-lookup"><span data-stu-id="176a7-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="176a7-176">`[IconImageName <String>]`: Nome amigável do usuário.</span><span class="sxs-lookup"><span data-stu-id="176a7-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="176a7-177">`[RawIcon <Byte[]>]`: o ícone de uma cadeia de caracteres de bit de 64 como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="176a7-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="176a7-178">`[RawPng <Byte[]>]`: o ícone de uma cadeia de caracteres de bit de 64 como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="176a7-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="176a7-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >: lista de dependências do pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="176a7-180">`[DependencyName <String>]`: Nome da dependência do pacote.</span><span class="sxs-lookup"><span data-stu-id="176a7-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="176a7-181">`[MinVersion <String>]`: Versão de dependência necessária.</span><span class="sxs-lookup"><span data-stu-id="176a7-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="176a7-182">`[Publisher <String>]`: Nome do fornecedor da dependência.</span><span class="sxs-lookup"><span data-stu-id="176a7-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="176a7-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="176a7-183">RELATED LINKS</span></span>

