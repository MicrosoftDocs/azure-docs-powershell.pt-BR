---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 9eba21106e5e2e7c22045d9aecdb86926e7e8ed7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772409"
---
# <span data-ttu-id="1e0ee-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="1e0ee-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="1e0ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0ee-103">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="1e0ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e0ee-104">SYNTAX</span></span>

### <span data-ttu-id="1e0ee-105">Automático</span><span class="sxs-lookup"><span data-stu-id="1e0ee-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e0ee-106">Manual</span><span class="sxs-lookup"><span data-stu-id="1e0ee-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e0ee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e0ee-107">DESCRIPTION</span></span>
<span data-ttu-id="1e0ee-108">Use **set-AzServiceFabricUpgradeType** para definir o tipo de atualização para automático ou manual com uma versão específica do código de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="1e0ee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e0ee-109">EXAMPLES</span></span>

### <span data-ttu-id="1e0ee-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e0ee-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="1e0ee-111">Esse comando definirá o modo de atualização do cluster como automático.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="1e0ee-112">OS</span><span class="sxs-lookup"><span data-stu-id="1e0ee-112">PARAMETERS</span></span>

### <span data-ttu-id="1e0ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0ee-113">-DefaultProfile</span></span>
<span data-ttu-id="1e0ee-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e0ee-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e0ee-115">-Name</span></span>
<span data-ttu-id="1e0ee-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="1e0ee-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e0ee-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1e0ee-119">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="1e0ee-119">-UpgradeMode</span></span>
<span data-ttu-id="1e0ee-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="1e0ee-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ee-121">-Versão</span><span class="sxs-lookup"><span data-stu-id="1e0ee-121">-Version</span></span>
<span data-ttu-id="1e0ee-122">Versão do código do cluster</span><span class="sxs-lookup"><span data-stu-id="1e0ee-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0ee-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e0ee-123">-Confirm</span></span>
<span data-ttu-id="1e0ee-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e0ee-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0ee-125">-WhatIf</span></span>
<span data-ttu-id="1e0ee-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e0ee-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e0ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0ee-128">CommonParameters</span></span>
<span data-ttu-id="1e0ee-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0ee-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e0ee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0ee-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e0ee-131">INPUTS</span></span>

### <span data-ttu-id="1e0ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e0ee-132">System.String</span></span>

### <span data-ttu-id="1e0ee-133">Microsoft. Azure. Commands. imfabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="1e0ee-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="1e0ee-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e0ee-134">OUTPUTS</span></span>

### <span data-ttu-id="1e0ee-135">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="1e0ee-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1e0ee-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e0ee-136">NOTES</span></span>

## <span data-ttu-id="1e0ee-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e0ee-137">RELATED LINKS</span></span>
