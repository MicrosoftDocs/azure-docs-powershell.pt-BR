---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429089"
---
# <span data-ttu-id="469a1-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="469a1-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="469a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="469a1-102">SYNOPSIS</span></span>
<span data-ttu-id="469a1-103">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="469a1-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="469a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="469a1-104">SYNTAX</span></span>

### <span data-ttu-id="469a1-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="469a1-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="469a1-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="469a1-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="469a1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="469a1-107">DESCRIPTION</span></span>
<span data-ttu-id="469a1-108">Use **Remove-AzureRmServiceFabricSetting** para remover as configurações do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="469a1-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="469a1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="469a1-109">EXAMPLES</span></span>

### <span data-ttu-id="469a1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="469a1-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="469a1-111">Este comando removerá as configurações ' MaxCursors ' na seção ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="469a1-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="469a1-112">OS</span><span class="sxs-lookup"><span data-stu-id="469a1-112">PARAMETERS</span></span>

### <span data-ttu-id="469a1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="469a1-113">-Name</span></span>
<span data-ttu-id="469a1-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="469a1-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="469a1-115">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="469a1-115">-Parameter</span></span>
<span data-ttu-id="469a1-116">Com.</span><span class="sxs-lookup"><span data-stu-id="469a1-116">Parameter.</span></span>

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

### <span data-ttu-id="469a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="469a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="469a1-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="469a1-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="469a1-119">-Seção</span><span class="sxs-lookup"><span data-stu-id="469a1-119">-Section</span></span>
<span data-ttu-id="469a1-120">Seção.</span><span class="sxs-lookup"><span data-stu-id="469a1-120">Section.</span></span>

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

### <span data-ttu-id="469a1-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="469a1-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="469a1-122">Tipo de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="469a1-122">Client authentication type.</span></span>

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

### <span data-ttu-id="469a1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="469a1-123">-Confirm</span></span>
<span data-ttu-id="469a1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="469a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469a1-125">-WhatIf</span></span>
<span data-ttu-id="469a1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="469a1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="469a1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="469a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469a1-128">-DefaultProfile</span></span>
<span data-ttu-id="469a1-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="469a1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="469a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469a1-130">CommonParameters</span></span>
<span data-ttu-id="469a1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469a1-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="469a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469a1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="469a1-133">INPUTS</span></span>

### <span data-ttu-id="469a1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="469a1-134">System.String</span></span>
<span data-ttu-id="469a1-135">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="469a1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="469a1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="469a1-136">OUTPUTS</span></span>

### <span data-ttu-id="469a1-137">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="469a1-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="469a1-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="469a1-138">NOTES</span></span>

## <span data-ttu-id="469a1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="469a1-139">RELATED LINKS</span></span>

