---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 7884e45c2b4f635c9236f213a93eb69524b37fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602405"
---
# <span data-ttu-id="29b90-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="29b90-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="29b90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29b90-102">SYNOPSIS</span></span>
<span data-ttu-id="29b90-103">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="29b90-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29b90-104">SYNTAX</span></span>

### <span data-ttu-id="29b90-105">Automático</span><span class="sxs-lookup"><span data-stu-id="29b90-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29b90-106">Manual</span><span class="sxs-lookup"><span data-stu-id="29b90-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b90-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29b90-107">DESCRIPTION</span></span>
<span data-ttu-id="29b90-108">Use **set-AzureRmServiceFabricUpgradeType** para definir o tipo de atualização para automático ou manual com uma versão específica do código de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="29b90-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="29b90-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29b90-109">EXAMPLES</span></span>

### <span data-ttu-id="29b90-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29b90-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="29b90-111">Esse comando definirá o modo de atualização do cluster como automático.</span><span class="sxs-lookup"><span data-stu-id="29b90-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="29b90-112">OS</span><span class="sxs-lookup"><span data-stu-id="29b90-112">PARAMETERS</span></span>

### <span data-ttu-id="29b90-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="29b90-113">-Name</span></span>
<span data-ttu-id="29b90-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="29b90-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="29b90-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b90-115">-ResourceGroupName</span></span>
<span data-ttu-id="29b90-116">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="29b90-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="29b90-117">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="29b90-117">-UpgradeMode</span></span>
<span data-ttu-id="29b90-118">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="29b90-118">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="29b90-119">-Versão</span><span class="sxs-lookup"><span data-stu-id="29b90-119">-Version</span></span>
<span data-ttu-id="29b90-120">Versão do código do cluster.</span><span class="sxs-lookup"><span data-stu-id="29b90-120">Cluster code version.</span></span>

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

### <span data-ttu-id="29b90-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29b90-121">-Confirm</span></span>
<span data-ttu-id="29b90-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29b90-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b90-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b90-123">-WhatIf</span></span>
<span data-ttu-id="29b90-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29b90-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29b90-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29b90-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b90-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b90-126">-DefaultProfile</span></span>
<span data-ttu-id="29b90-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29b90-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29b90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b90-128">CommonParameters</span></span>
<span data-ttu-id="29b90-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b90-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b90-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b90-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29b90-131">INPUTS</span></span>

### <span data-ttu-id="29b90-132">Microsoft. Azure. Commands. imfabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="29b90-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="29b90-133">System. String</span><span class="sxs-lookup"><span data-stu-id="29b90-133">System.String</span></span>

## <span data-ttu-id="29b90-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29b90-134">OUTPUTS</span></span>

### <span data-ttu-id="29b90-135">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="29b90-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="29b90-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29b90-136">NOTES</span></span>

## <span data-ttu-id="29b90-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29b90-137">RELATED LINKS</span></span>

