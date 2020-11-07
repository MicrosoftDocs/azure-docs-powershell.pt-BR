---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69fa98b75b6897355b34ba91a39196f072d6af6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773193"
---
# <span data-ttu-id="106bd-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="106bd-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="106bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="106bd-102">SYNOPSIS</span></span>
<span data-ttu-id="106bd-103">Crie uma nova versão do tipo de aplicativo no grupo de recursos e no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="106bd-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="106bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="106bd-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="106bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="106bd-105">DESCRIPTION</span></span>
<span data-ttu-id="106bd-106">Esse cmdlet cria uma nova versão de tipo de aplicativo usando o pacote especificado em-PackageUrl, isso deve ser acessível por meio de um ponto de extremidade REST para o Azure Resource Manager para consumir durante a implantação e conter o aplicativo empacotado e compactado com a extensão. sfpkg.</span><span class="sxs-lookup"><span data-stu-id="106bd-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="106bd-107">Esse comando criará o tipo de aplicativo, se ele ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="106bd-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="106bd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="106bd-108">EXAMPLES</span></span>

### <span data-ttu-id="106bd-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="106bd-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="106bd-110">Este exemplo criará um tipo de aplicativo versão "v1" em tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="106bd-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="106bd-111">A versão no manifesto do aplicativo contida no pacote deve ter a mesma versão que a especificada na versão.</span><span class="sxs-lookup"><span data-stu-id="106bd-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="106bd-112">OS</span><span class="sxs-lookup"><span data-stu-id="106bd-112">PARAMETERS</span></span>

### <span data-ttu-id="106bd-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="106bd-113">-ClusterName</span></span>
<span data-ttu-id="106bd-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="106bd-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="106bd-115">-Defaultparameter</span><span class="sxs-lookup"><span data-stu-id="106bd-115">-DefaultParameter</span></span>
<span data-ttu-id="106bd-116">Especifique os valores padrão dos parâmetros do aplicativo como pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="106bd-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="106bd-117">Esses parâmetros devem existir no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="106bd-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="106bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106bd-118">-DefaultProfile</span></span>
<span data-ttu-id="106bd-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="106bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106bd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="106bd-120">-Force</span></span>
<span data-ttu-id="106bd-121">Continuar sem confirmação</span><span class="sxs-lookup"><span data-stu-id="106bd-121">Continue without prompts</span></span>

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

### <span data-ttu-id="106bd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="106bd-122">-Name</span></span>
<span data-ttu-id="106bd-123">Especificar o nome do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="106bd-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="106bd-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="106bd-124">-PackageUrl</span></span>
<span data-ttu-id="106bd-125">Especificar a URL do arquivo de pacote do aplicativo sfpkg</span><span class="sxs-lookup"><span data-stu-id="106bd-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="106bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="106bd-127">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="106bd-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="106bd-128">-Versão</span><span class="sxs-lookup"><span data-stu-id="106bd-128">-Version</span></span>
<span data-ttu-id="106bd-129">Especificar a versão do tipo de aplicativo</span><span class="sxs-lookup"><span data-stu-id="106bd-129">Specify the application type version</span></span>

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

### <span data-ttu-id="106bd-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="106bd-130">-Confirm</span></span>
<span data-ttu-id="106bd-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="106bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="106bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106bd-132">-WhatIf</span></span>
<span data-ttu-id="106bd-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="106bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="106bd-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="106bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="106bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106bd-135">CommonParameters</span></span>
<span data-ttu-id="106bd-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106bd-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106bd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106bd-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="106bd-138">INPUTS</span></span>

### <span data-ttu-id="106bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="106bd-139">System.String</span></span>

### <span data-ttu-id="106bd-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="106bd-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="106bd-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="106bd-141">OUTPUTS</span></span>

### <span data-ttu-id="106bd-142">Microsoft. Azure. Commands. imfabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="106bd-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="106bd-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="106bd-143">NOTES</span></span>

## <span data-ttu-id="106bd-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="106bd-144">RELATED LINKS</span></span>