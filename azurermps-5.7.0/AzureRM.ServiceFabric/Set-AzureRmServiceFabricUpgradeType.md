---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433407"
---
# <span data-ttu-id="2646f-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="2646f-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="2646f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2646f-102">SYNOPSIS</span></span>
<span data-ttu-id="2646f-103">Altere o tipo de atualização do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="2646f-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2646f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2646f-104">SYNTAX</span></span>

### <span data-ttu-id="2646f-105">Automático</span><span class="sxs-lookup"><span data-stu-id="2646f-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2646f-106">Manual</span><span class="sxs-lookup"><span data-stu-id="2646f-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2646f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2646f-107">DESCRIPTION</span></span>
<span data-ttu-id="2646f-108">Use **set-AzureRmServiceFabricUpgradeType** para definir o tipo de atualização para automático ou manual com uma versão específica do código de malha de serviço.</span><span class="sxs-lookup"><span data-stu-id="2646f-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="2646f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2646f-109">EXAMPLES</span></span>

### <span data-ttu-id="2646f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2646f-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="2646f-111">Esse comando definirá o modo de atualização do cluster como automático.</span><span class="sxs-lookup"><span data-stu-id="2646f-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="2646f-112">OS</span><span class="sxs-lookup"><span data-stu-id="2646f-112">PARAMETERS</span></span>

### <span data-ttu-id="2646f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2646f-113">-DefaultProfile</span></span>
<span data-ttu-id="2646f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2646f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2646f-115">-Name</span></span>
<span data-ttu-id="2646f-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2646f-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2646f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2646f-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2646f-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-119">-Upgrademode</span><span class="sxs-lookup"><span data-stu-id="2646f-119">-UpgradeMode</span></span>
<span data-ttu-id="2646f-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="2646f-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-121">-Versão</span><span class="sxs-lookup"><span data-stu-id="2646f-121">-Version</span></span>
<span data-ttu-id="2646f-122">Versão do código do cluster.</span><span class="sxs-lookup"><span data-stu-id="2646f-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2646f-123">-Confirm</span></span>
<span data-ttu-id="2646f-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2646f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2646f-125">-WhatIf</span></span>
<span data-ttu-id="2646f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2646f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2646f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2646f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2646f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2646f-128">CommonParameters</span></span>
<span data-ttu-id="2646f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2646f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2646f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2646f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2646f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2646f-131">INPUTS</span></span>

### <span data-ttu-id="2646f-132">Microsoft. Azure. Commands. imfabric. Models. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="2646f-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="2646f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2646f-133">System.String</span></span>

## <span data-ttu-id="2646f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2646f-134">OUTPUTS</span></span>

### <span data-ttu-id="2646f-135">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="2646f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="2646f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2646f-136">NOTES</span></span>

## <span data-ttu-id="2646f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2646f-137">RELATED LINKS</span></span>

