---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116168"
---
# <span data-ttu-id="29904-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="29904-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="29904-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29904-102">SYNOPSIS</span></span>
<span data-ttu-id="29904-103">Altere o tipo de atualização de Malha de Serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="29904-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="29904-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29904-104">SYNTAX</span></span>

### <span data-ttu-id="29904-105">Automático</span><span class="sxs-lookup"><span data-stu-id="29904-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29904-106">Manual</span><span class="sxs-lookup"><span data-stu-id="29904-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29904-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="29904-107">DESCRIPTION</span></span>
<span data-ttu-id="29904-108">Use **Set-AzServiceFabricUpgradeType** para definir o tipo de atualização como automático ou manual com uma versão de código de Malha de Serviço específica.</span><span class="sxs-lookup"><span data-stu-id="29904-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="29904-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29904-109">EXAMPLES</span></span>

### <span data-ttu-id="29904-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29904-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="29904-111">Esse comando definirá o modo de atualização de cluster como automático.</span><span class="sxs-lookup"><span data-stu-id="29904-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="29904-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29904-112">PARAMETERS</span></span>

### <span data-ttu-id="29904-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29904-113">-DefaultProfile</span></span>
<span data-ttu-id="29904-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29904-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29904-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="29904-115">-Name</span></span>
<span data-ttu-id="29904-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="29904-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="29904-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29904-117">-ResourceGroupName</span></span>
<span data-ttu-id="29904-118">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29904-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="29904-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="29904-119">-UpgradeMode</span></span>
<span data-ttu-id="29904-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="29904-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="29904-121">-Versão</span><span class="sxs-lookup"><span data-stu-id="29904-121">-Version</span></span>
<span data-ttu-id="29904-122">Versão de código de cluster</span><span class="sxs-lookup"><span data-stu-id="29904-122">Cluster code version</span></span>

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

### <span data-ttu-id="29904-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="29904-123">-Confirm</span></span>
<span data-ttu-id="29904-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29904-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29904-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29904-125">-WhatIf</span></span>
<span data-ttu-id="29904-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="29904-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29904-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29904-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29904-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29904-128">CommonParameters</span></span>
<span data-ttu-id="29904-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29904-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29904-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29904-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29904-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="29904-131">INPUTS</span></span>

### <span data-ttu-id="29904-132">System.String</span><span class="sxs-lookup"><span data-stu-id="29904-132">System.String</span></span>

### <span data-ttu-id="29904-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="29904-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="29904-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="29904-134">OUTPUTS</span></span>

### <span data-ttu-id="29904-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="29904-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="29904-136">Notas</span><span class="sxs-lookup"><span data-stu-id="29904-136">NOTES</span></span>

## <span data-ttu-id="29904-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29904-137">RELATED LINKS</span></span>
