---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116380"
---
# <span data-ttu-id="9391b-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9391b-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="9391b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9391b-102">SYNOPSIS</span></span>
<span data-ttu-id="9391b-103">Crie uma nova versão de tipo de aplicativo sob o grupo de recursos e cluster especificados.</span><span class="sxs-lookup"><span data-stu-id="9391b-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="9391b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9391b-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9391b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9391b-105">DESCRIPTION</span></span>
<span data-ttu-id="9391b-106">Este cmdlet cria uma nova versão de tipo de aplicativo usando o pacote especificado em -PackageUrl, ele deve estar acessível por meio de um ponto de extremidade REST para que o Gerenciador de Recursos do Azure seja consumido durante a implantação e continha o aplicativo empacotado e cortado com a extensão .sfpkg.</span><span class="sxs-lookup"><span data-stu-id="9391b-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="9391b-107">Esse comando criará o tipo de aplicativo se ele ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="9391b-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="9391b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9391b-108">EXAMPLES</span></span>

### <span data-ttu-id="9391b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9391b-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="9391b-110">Este exemplo criará uma versão de tipo de aplicativo "v1" em tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="9391b-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="9391b-111">A versão no manifesto do aplicativo contida no pacote deve ter a mesma versão especificada em -Version.</span><span class="sxs-lookup"><span data-stu-id="9391b-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="9391b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9391b-112">PARAMETERS</span></span>

### <span data-ttu-id="9391b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9391b-113">-ClusterName</span></span>
<span data-ttu-id="9391b-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="9391b-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9391b-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="9391b-115">-DefaultParameter</span></span>
<span data-ttu-id="9391b-116">Especifique os valores padrão dos parâmetros de aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="9391b-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="9391b-117">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9391b-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="9391b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9391b-118">-DefaultProfile</span></span>
<span data-ttu-id="9391b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9391b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9391b-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9391b-120">-Force</span></span>
<span data-ttu-id="9391b-121">Continuar sem avisos</span><span class="sxs-lookup"><span data-stu-id="9391b-121">Continue without prompts</span></span>

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

### <span data-ttu-id="9391b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9391b-122">-Name</span></span>
<span data-ttu-id="9391b-123">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9391b-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9391b-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="9391b-124">-PackageUrl</span></span>
<span data-ttu-id="9391b-125">Especificar a url do arquivo de sfpkg do pacote de aplicativos</span><span class="sxs-lookup"><span data-stu-id="9391b-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9391b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9391b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9391b-127">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9391b-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9391b-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="9391b-128">-Version</span></span>
<span data-ttu-id="9391b-129">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9391b-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9391b-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9391b-130">-Confirm</span></span>
<span data-ttu-id="9391b-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9391b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9391b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9391b-132">-WhatIf</span></span>
<span data-ttu-id="9391b-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9391b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9391b-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9391b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9391b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9391b-135">CommonParameters</span></span>
<span data-ttu-id="9391b-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9391b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9391b-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9391b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9391b-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="9391b-138">INPUTS</span></span>

### <span data-ttu-id="9391b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9391b-139">System.String</span></span>

### <span data-ttu-id="9391b-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9391b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9391b-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="9391b-141">OUTPUTS</span></span>

### <span data-ttu-id="9391b-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9391b-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="9391b-143">Notas</span><span class="sxs-lookup"><span data-stu-id="9391b-143">NOTES</span></span>

## <span data-ttu-id="9391b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9391b-144">RELATED LINKS</span></span>
