---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429088"
---
# <span data-ttu-id="07625-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="07625-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="07625-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07625-102">SYNOPSIS</span></span>
<span data-ttu-id="07625-103">Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.</span><span class="sxs-lookup"><span data-stu-id="07625-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07625-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07625-104">SYNTAX</span></span>

### <span data-ttu-id="07625-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="07625-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07625-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="07625-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07625-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07625-107">DESCRIPTION</span></span>
<span data-ttu-id="07625-108">Use **set-AzureRmServiceFabricSetting** para adicionar ou atualizar as configurações do Service Fabric em um cluster.</span><span class="sxs-lookup"><span data-stu-id="07625-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="07625-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07625-109">EXAMPLES</span></span>

### <span data-ttu-id="07625-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07625-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="07625-111">Esse comando definirá ' MaxFileOperationTimeout ' como o valor ' 5000 ' na seção ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="07625-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="07625-112">OS</span><span class="sxs-lookup"><span data-stu-id="07625-112">PARAMETERS</span></span>

### <span data-ttu-id="07625-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="07625-113">-Name</span></span>
<span data-ttu-id="07625-114">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="07625-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="07625-115">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="07625-115">-Parameter</span></span>
<span data-ttu-id="07625-116">Com.</span><span class="sxs-lookup"><span data-stu-id="07625-116">Parameter.</span></span>

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

### <span data-ttu-id="07625-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07625-117">-ResourceGroupName</span></span>
<span data-ttu-id="07625-118">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07625-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="07625-119">-Seção</span><span class="sxs-lookup"><span data-stu-id="07625-119">-Section</span></span>
<span data-ttu-id="07625-120">Seção.</span><span class="sxs-lookup"><span data-stu-id="07625-120">Section.</span></span>

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

### <span data-ttu-id="07625-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="07625-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="07625-122">Tipo de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="07625-122">Client authentication type.</span></span>

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

### <span data-ttu-id="07625-123">-Valor</span><span class="sxs-lookup"><span data-stu-id="07625-123">-Value</span></span>
<span data-ttu-id="07625-124">Valores.</span><span class="sxs-lookup"><span data-stu-id="07625-124">Value.</span></span>

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

### <span data-ttu-id="07625-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07625-125">-Confirm</span></span>
<span data-ttu-id="07625-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07625-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07625-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07625-127">-WhatIf</span></span>
<span data-ttu-id="07625-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07625-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07625-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07625-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07625-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07625-130">-DefaultProfile</span></span>
<span data-ttu-id="07625-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07625-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07625-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07625-132">CommonParameters</span></span>
<span data-ttu-id="07625-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07625-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07625-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07625-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07625-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07625-135">INPUTS</span></span>

### <span data-ttu-id="07625-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07625-136">System.String</span></span>
<span data-ttu-id="07625-137">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="07625-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="07625-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07625-138">OUTPUTS</span></span>

### <span data-ttu-id="07625-139">Microsoft. Azure. Commands. imfabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="07625-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="07625-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07625-140">NOTES</span></span>

## <span data-ttu-id="07625-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07625-141">RELATED LINKS</span></span>
