---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610057"
---
# <span data-ttu-id="aee1e-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="aee1e-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="aee1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aee1e-102">SYNOPSIS</span></span>
<span data-ttu-id="aee1e-103">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="aee1e-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aee1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aee1e-104">SYNTAX</span></span>

### <span data-ttu-id="aee1e-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="aee1e-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aee1e-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="aee1e-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aee1e-107">DESCRIPTION</span></span>
<span data-ttu-id="aee1e-108">Use **Remove-AzureRmServiceFabricSetting** para remover as configurações do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="aee1e-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="aee1e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aee1e-109">EXAMPLES</span></span>

### <span data-ttu-id="aee1e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aee1e-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="aee1e-111">Este comando removerá as configurações ' MaxCursors ' na seção ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="aee1e-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="aee1e-112">OS</span><span class="sxs-lookup"><span data-stu-id="aee1e-112">PARAMETERS</span></span>

### <span data-ttu-id="aee1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee1e-113">-DefaultProfile</span></span>
<span data-ttu-id="aee1e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aee1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aee1e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="aee1e-115">-Name</span></span>
<span data-ttu-id="aee1e-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="aee1e-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="aee1e-117">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="aee1e-117">-Parameter</span></span>
<span data-ttu-id="aee1e-118">Com.</span><span class="sxs-lookup"><span data-stu-id="aee1e-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee1e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aee1e-119">-ResourceGroupName</span></span>
<span data-ttu-id="aee1e-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aee1e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aee1e-121">-Seção</span><span class="sxs-lookup"><span data-stu-id="aee1e-121">-Section</span></span>
<span data-ttu-id="aee1e-122">Seção.</span><span class="sxs-lookup"><span data-stu-id="aee1e-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee1e-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="aee1e-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="aee1e-124">Tipo de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="aee1e-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aee1e-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aee1e-125">-Confirm</span></span>
<span data-ttu-id="aee1e-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aee1e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee1e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee1e-127">-WhatIf</span></span>
<span data-ttu-id="aee1e-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aee1e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aee1e-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aee1e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee1e-130">CommonParameters</span></span>
<span data-ttu-id="aee1e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aee1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee1e-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aee1e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee1e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aee1e-133">INPUTS</span></span>

### <span data-ttu-id="aee1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aee1e-134">System.String</span></span>
<span data-ttu-id="aee1e-135">Parâmetros: Parameter (ByValue), seção (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aee1e-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="aee1e-136">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="aee1e-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="aee1e-137">Parâmetros: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aee1e-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="aee1e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aee1e-138">OUTPUTS</span></span>

### <span data-ttu-id="aee1e-139">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="aee1e-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="aee1e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aee1e-140">NOTES</span></span>

## <span data-ttu-id="aee1e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aee1e-141">RELATED LINKS</span></span>
