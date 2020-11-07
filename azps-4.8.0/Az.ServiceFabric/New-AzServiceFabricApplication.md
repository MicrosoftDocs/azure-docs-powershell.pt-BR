---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954667"
---
# <span data-ttu-id="42e62-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="42e62-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="42e62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42e62-102">SYNOPSIS</span></span>
<span data-ttu-id="42e62-103">Criar novo aplicativo Service Fabric no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="42e62-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="42e62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42e62-104">SYNTAX</span></span>

### <span data-ttu-id="42e62-105">SkipAppTypeVersion (padrão)</span><span class="sxs-lookup"><span data-stu-id="42e62-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42e62-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="42e62-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42e62-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42e62-107">DESCRIPTION</span></span>
<span data-ttu-id="42e62-108">Esse cmdlet cria um novo aplicativo de malha de serviços no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="42e62-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="42e62-109">O parâmetro-PackageUrl pode ser usado para criar a versão do tipo, se a versão do tipo já estiver sendo encerrada, mas seu estado in ' Failed ', o cmdlet perguntará se o usuário deseja recriar a versão do tipo.</span><span class="sxs-lookup"><span data-stu-id="42e62-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="42e62-110">Se continuar no estado ' falha ', o comando irá parar o processo e gerar uma exceção.</span><span class="sxs-lookup"><span data-stu-id="42e62-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="42e62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42e62-111">EXAMPLES</span></span>

### <span data-ttu-id="42e62-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="42e62-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="42e62-113">Este exemplo cria o aplicativo "testApp" em grupo de recursos "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="42e62-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="42e62-114">O tipo de aplicativo "TestAppType" versão "v1" já deve existir no cluster, e os parâmetros do aplicativo devem ser definidos no manifesto do aplicativo, caso contrário, o cmdlet irá falhar.</span><span class="sxs-lookup"><span data-stu-id="42e62-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="42e62-115">Exemplo 2: especificar-PackageUrl para criar a versão do tipo de aplicativo antes de criar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42e62-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="42e62-116">Este exemplo cria o tipo de aplicativo "TestAppType" versão "v1" usando a URL do pacote fornecida.</span><span class="sxs-lookup"><span data-stu-id="42e62-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="42e62-117">Depois disso, ele vai continuar o processo normal para criar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42e62-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="42e62-118">Se a versão do tipo de aplicativo já estiver sendo encerrada e o estado de provisionamento que estava em ' Failed ', ele solicitará que ele decida se o usuário quer recriar a versão do tipo.</span><span class="sxs-lookup"><span data-stu-id="42e62-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="42e62-119">OS</span><span class="sxs-lookup"><span data-stu-id="42e62-119">PARAMETERS</span></span>

### <span data-ttu-id="42e62-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="42e62-120">-ApplicationParameter</span></span>
<span data-ttu-id="42e62-121">Especifique os parâmetros do aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="42e62-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="42e62-122">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42e62-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="42e62-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="42e62-123">-ApplicationTypeName</span></span>
<span data-ttu-id="42e62-124">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="42e62-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="42e62-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="42e62-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="42e62-126">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="42e62-126">Specify the application type version</span></span>

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

### <span data-ttu-id="42e62-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="42e62-127">-ClusterName</span></span>
<span data-ttu-id="42e62-128">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="42e62-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="42e62-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e62-129">-DefaultProfile</span></span>
<span data-ttu-id="42e62-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42e62-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e62-131">-Force</span><span class="sxs-lookup"><span data-stu-id="42e62-131">-Force</span></span>
<span data-ttu-id="42e62-132">Continuar sem confirmação</span><span class="sxs-lookup"><span data-stu-id="42e62-132">Continue without prompts</span></span>

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

### <span data-ttu-id="42e62-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="42e62-133">-MaximumNodeCount</span></span>
<span data-ttu-id="42e62-134">Especifica o número máximo de nós nos quais colocar um aplicativo</span><span class="sxs-lookup"><span data-stu-id="42e62-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="42e62-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="42e62-135">-MinimumNodeCount</span></span>
<span data-ttu-id="42e62-136">Especifica o número mínimo de nós em que o Service Fabric reservará capacidade para este aplicativo</span><span class="sxs-lookup"><span data-stu-id="42e62-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="42e62-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="42e62-137">-Name</span></span>
<span data-ttu-id="42e62-138">Especificar o nome do aplicativo</span><span class="sxs-lookup"><span data-stu-id="42e62-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="42e62-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="42e62-139">-PackageUrl</span></span>
<span data-ttu-id="42e62-140">Especificar a URL do arquivo de pacote do aplicativo sfpkg</span><span class="sxs-lookup"><span data-stu-id="42e62-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="42e62-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e62-141">-ResourceGroupName</span></span>
<span data-ttu-id="42e62-142">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42e62-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="42e62-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42e62-143">-Confirm</span></span>
<span data-ttu-id="42e62-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42e62-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42e62-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42e62-145">-WhatIf</span></span>
<span data-ttu-id="42e62-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42e62-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42e62-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42e62-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42e62-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e62-148">CommonParameters</span></span>
<span data-ttu-id="42e62-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e62-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e62-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e62-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e62-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42e62-151">INPUTS</span></span>

### <span data-ttu-id="42e62-152">System. String</span><span class="sxs-lookup"><span data-stu-id="42e62-152">System.String</span></span>

### <span data-ttu-id="42e62-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="42e62-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="42e62-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42e62-154">OUTPUTS</span></span>

### <span data-ttu-id="42e62-155">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="42e62-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="42e62-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42e62-156">NOTES</span></span>

## <span data-ttu-id="42e62-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42e62-157">RELATED LINKS</span></span>
