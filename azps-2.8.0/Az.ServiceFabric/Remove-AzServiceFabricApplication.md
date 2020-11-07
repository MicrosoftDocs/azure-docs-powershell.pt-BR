---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 1ad1e8220ed77a9206503adaf4f9924f95fe4f44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773190"
---
# <span data-ttu-id="c0879-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c0879-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c0879-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0879-102">SYNOPSIS</span></span>
<span data-ttu-id="c0879-103">Remover um aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="c0879-103">Remove an application from the cluster.</span></span> <span data-ttu-id="c0879-104">Isso removerá todos os serviços do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0879-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="c0879-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0879-105">SYNTAX</span></span>

### <span data-ttu-id="c0879-106">ByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0879-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0879-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0879-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0879-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0879-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0879-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0879-109">DESCRIPTION</span></span>
<span data-ttu-id="c0879-110">Esse cmdlet Remove um formulário de aplicativo do cluster.</span><span class="sxs-lookup"><span data-stu-id="c0879-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="c0879-111">Isso removerá todos os serviços, se houver, sob o recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0879-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="c0879-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0879-112">EXAMPLES</span></span>

### <span data-ttu-id="c0879-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0879-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c0879-114">Este exemplo remove o aplicativo "testApp" no grupo de recursos "testRG" e cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="c0879-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="c0879-115">OS</span><span class="sxs-lookup"><span data-stu-id="c0879-115">PARAMETERS</span></span>

### <span data-ttu-id="c0879-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0879-116">-ClusterName</span></span>
<span data-ttu-id="c0879-117">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c0879-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c0879-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0879-118">-DefaultProfile</span></span>
<span data-ttu-id="c0879-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0879-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0879-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c0879-120">-Force</span></span>
<span data-ttu-id="c0879-121">Remover sem aviso.</span><span class="sxs-lookup"><span data-stu-id="c0879-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="c0879-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0879-122">-InputObject</span></span>
<span data-ttu-id="c0879-123">O recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0879-123">The application resource.</span></span>

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

### <span data-ttu-id="c0879-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0879-124">-Name</span></span>
<span data-ttu-id="c0879-125">Especifique o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0879-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c0879-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0879-126">-PassThru</span></span>
<span data-ttu-id="c0879-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="c0879-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c0879-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0879-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0879-129">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0879-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c0879-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0879-130">-ResourceId</span></span>
<span data-ttu-id="c0879-131">Resourcebinding do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0879-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c0879-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0879-132">-Confirm</span></span>
<span data-ttu-id="c0879-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0879-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0879-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0879-134">-WhatIf</span></span>
<span data-ttu-id="c0879-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0879-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0879-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0879-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0879-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0879-137">CommonParameters</span></span>
<span data-ttu-id="c0879-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0879-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0879-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0879-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0879-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0879-140">INPUTS</span></span>

### <span data-ttu-id="c0879-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c0879-141">System.String</span></span>

### <span data-ttu-id="c0879-142">Microsoft. Azure. Commands. imfabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c0879-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c0879-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0879-143">OUTPUTS</span></span>

### <span data-ttu-id="c0879-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0879-144">System.Boolean</span></span>

## <span data-ttu-id="c0879-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0879-145">NOTES</span></span>

## <span data-ttu-id="c0879-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0879-146">RELATED LINKS</span></span>