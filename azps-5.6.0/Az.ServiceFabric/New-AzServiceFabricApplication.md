---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889156"
---
# <span data-ttu-id="46eff-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46eff-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="46eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46eff-102">SYNOPSIS</span></span>
<span data-ttu-id="46eff-103">Crie um novo aplicativo de malha de serviço sob o grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="46eff-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="46eff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46eff-104">SYNTAX</span></span>

### <span data-ttu-id="46eff-105">SkipAppTypeVersion (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46eff-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46eff-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46eff-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46eff-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46eff-107">DESCRIPTION</span></span>
<span data-ttu-id="46eff-108">Este cmdlet cria um novo aplicativo de malha de serviço sob o grupo de recursos especificado e o cluster.</span><span class="sxs-lookup"><span data-stu-id="46eff-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="46eff-109">O parâmetro -PackageUrl pode ser usado para criar a versão de tipo, Se a versão de tipo já sair, mas estiver em estado 'Falha', o cmdlet perguntará se o usuário deseja recriar a versão de tipo.</span><span class="sxs-lookup"><span data-stu-id="46eff-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="46eff-110">Se ele continuar no estado 'Falha', o comando interromperá o processo e lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="46eff-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="46eff-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46eff-111">EXAMPLES</span></span>

### <span data-ttu-id="46eff-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46eff-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="46eff-113">Este exemplo cria o aplicativo "testApp" em grupo de recursos "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="46eff-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="46eff-114">O tipo de aplicativo "TestAppType" versão "v1" já deve existir no cluster, e os parâmetros de aplicativo devem ser definidos no manifesto do aplicativo caso contrário, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="46eff-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="46eff-115">Exemplo 2: Especifique -PackageUrl para criar a versão do tipo de aplicativo antes de criar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46eff-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="46eff-116">Este exemplo cria o tipo de aplicativo "TestAppType" versão "v1" usando a url do pacote fornecida.</span><span class="sxs-lookup"><span data-stu-id="46eff-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="46eff-117">Depois disso, ele continuará o processo normal para criar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46eff-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="46eff-118">Se a versão do tipo de aplicativo já sair e o estado de provisionamento estiver em 'Falha' ele solicitará que decida se o usuário deseja recriar a versão de tipo.</span><span class="sxs-lookup"><span data-stu-id="46eff-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="46eff-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46eff-119">PARAMETERS</span></span>

### <span data-ttu-id="46eff-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="46eff-120">-ApplicationParameter</span></span>
<span data-ttu-id="46eff-121">Especifique os parâmetros do aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="46eff-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="46eff-122">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46eff-122">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="46eff-123">-ApplicationTypeName</span></span>
<span data-ttu-id="46eff-124">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="46eff-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46eff-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="46eff-126">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="46eff-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="46eff-127">-ClusterName</span></span>
<span data-ttu-id="46eff-128">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="46eff-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46eff-129">-DefaultProfile</span></span>
<span data-ttu-id="46eff-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46eff-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46eff-131">-Force</span><span class="sxs-lookup"><span data-stu-id="46eff-131">-Force</span></span>
<span data-ttu-id="46eff-132">Continuar sem prompts</span><span class="sxs-lookup"><span data-stu-id="46eff-132">Continue without prompts</span></span>

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

### <span data-ttu-id="46eff-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="46eff-133">-MaximumNodeCount</span></span>
<span data-ttu-id="46eff-134">Especifica o número máximo de nós nos quais colocar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="46eff-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="46eff-135">-MinimumNodeCount</span></span>
<span data-ttu-id="46eff-136">Especifica o número mínimo de nós onde o Service Fabric reservará capacidade para este aplicativo</span><span class="sxs-lookup"><span data-stu-id="46eff-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-137">-Name</span><span class="sxs-lookup"><span data-stu-id="46eff-137">-Name</span></span>
<span data-ttu-id="46eff-138">Especificar o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="46eff-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="46eff-139">-PackageUrl</span></span>
<span data-ttu-id="46eff-140">Especificar a url do arquivo sfpkg do pacote de aplicativos</span><span class="sxs-lookup"><span data-stu-id="46eff-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46eff-141">-ResourceGroupName</span></span>
<span data-ttu-id="46eff-142">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46eff-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46eff-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46eff-143">-Confirm</span></span>
<span data-ttu-id="46eff-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46eff-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46eff-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46eff-145">-WhatIf</span></span>
<span data-ttu-id="46eff-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46eff-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46eff-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46eff-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46eff-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46eff-148">CommonParameters</span></span>
<span data-ttu-id="46eff-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46eff-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46eff-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46eff-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46eff-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46eff-151">INPUTS</span></span>

### <span data-ttu-id="46eff-152">System.String</span><span class="sxs-lookup"><span data-stu-id="46eff-152">System.String</span></span>

### <span data-ttu-id="46eff-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46eff-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46eff-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46eff-154">OUTPUTS</span></span>

### <span data-ttu-id="46eff-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="46eff-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="46eff-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="46eff-156">NOTES</span></span>

## <span data-ttu-id="46eff-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46eff-157">RELATED LINKS</span></span>
