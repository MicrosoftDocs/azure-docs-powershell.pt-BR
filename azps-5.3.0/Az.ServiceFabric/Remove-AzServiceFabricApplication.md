---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433032"
---
# <span data-ttu-id="6614f-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6614f-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="6614f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6614f-102">SYNOPSIS</span></span>
<span data-ttu-id="6614f-103">Remover um aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="6614f-103">Remove an application from the cluster.</span></span> <span data-ttu-id="6614f-104">Isso removerá todos os serviços do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6614f-104">This will remove all the services under the application.</span></span> <span data-ttu-id="6614f-105">Só oferece suporte a aplicativos de ARM distribuído.</span><span class="sxs-lookup"><span data-stu-id="6614f-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="6614f-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6614f-106">SYNTAX</span></span>

### <span data-ttu-id="6614f-107">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="6614f-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6614f-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6614f-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6614f-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6614f-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6614f-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6614f-110">DESCRIPTION</span></span>
<span data-ttu-id="6614f-111">Esse cmdlet Remove um formulário de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="6614f-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="6614f-112">Isso removerá todos os serviços, se houver, sob o recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6614f-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="6614f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6614f-113">EXAMPLES</span></span>

### <span data-ttu-id="6614f-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6614f-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="6614f-115">Este exemplo remove o aplicativo "testApp" no grupo de recursos "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="6614f-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="6614f-116">OS</span><span class="sxs-lookup"><span data-stu-id="6614f-116">PARAMETERS</span></span>

### <span data-ttu-id="6614f-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6614f-117">-ClusterName</span></span>
<span data-ttu-id="6614f-118">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="6614f-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6614f-119">-DefaultProfile</span></span>
<span data-ttu-id="6614f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6614f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6614f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6614f-121">-Force</span></span>
<span data-ttu-id="6614f-122">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="6614f-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="6614f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6614f-123">-InputObject</span></span>
<span data-ttu-id="6614f-124">O recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6614f-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6614f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6614f-125">-Name</span></span>
<span data-ttu-id="6614f-126">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6614f-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6614f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6614f-127">-PassThru</span></span>
<span data-ttu-id="6614f-128">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="6614f-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6614f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6614f-129">-ResourceGroupName</span></span>
<span data-ttu-id="6614f-130">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6614f-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6614f-131">-ResourceId</span></span>
<span data-ttu-id="6614f-132">Resourcebinding do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6614f-132">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6614f-133">-Confirm</span></span>
<span data-ttu-id="6614f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6614f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6614f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6614f-135">-WhatIf</span></span>
<span data-ttu-id="6614f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6614f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6614f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6614f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6614f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6614f-138">CommonParameters</span></span>
<span data-ttu-id="6614f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6614f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6614f-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6614f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6614f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6614f-141">INPUTS</span></span>

### <span data-ttu-id="6614f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6614f-142">System.String</span></span>

### <span data-ttu-id="6614f-143">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="6614f-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="6614f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6614f-144">OUTPUTS</span></span>

### <span data-ttu-id="6614f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6614f-145">System.Boolean</span></span>

## <span data-ttu-id="6614f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6614f-146">NOTES</span></span>

## <span data-ttu-id="6614f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6614f-147">RELATED LINKS</span></span>
