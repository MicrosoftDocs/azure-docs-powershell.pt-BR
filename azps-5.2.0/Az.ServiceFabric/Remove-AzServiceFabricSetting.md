---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: db6d94b4aa2f6182abc114f11d1dba0b40ebbb93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257792"
---
# <span data-ttu-id="79115-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="79115-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="79115-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79115-102">SYNOPSIS</span></span>
<span data-ttu-id="79115-103">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="79115-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="79115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79115-104">SYNTAX</span></span>

### <span data-ttu-id="79115-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="79115-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79115-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="79115-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79115-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79115-107">DESCRIPTION</span></span>
<span data-ttu-id="79115-108">Use **Remove-AzServiceFabricSetting** para remover as configurações do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="79115-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="79115-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79115-109">EXAMPLES</span></span>

### <span data-ttu-id="79115-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79115-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="79115-111">Este comando removerá as configurações ' MaxCursors ' na seção ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="79115-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="79115-112">OS</span><span class="sxs-lookup"><span data-stu-id="79115-112">PARAMETERS</span></span>

### <span data-ttu-id="79115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79115-113">-DefaultProfile</span></span>
<span data-ttu-id="79115-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79115-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79115-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="79115-115">-Name</span></span>
<span data-ttu-id="79115-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="79115-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="79115-117">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="79115-117">-Parameter</span></span>
<span data-ttu-id="79115-118">Nome do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="79115-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="79115-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79115-119">-ResourceGroupName</span></span>
<span data-ttu-id="79115-120">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="79115-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="79115-121">-Seção</span><span class="sxs-lookup"><span data-stu-id="79115-121">-Section</span></span>
<span data-ttu-id="79115-122">Nome da seção da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="79115-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="79115-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="79115-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="79115-124">Uma matriz de configurações da malha</span><span class="sxs-lookup"><span data-stu-id="79115-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="79115-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79115-125">-Confirm</span></span>
<span data-ttu-id="79115-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79115-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79115-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79115-127">-WhatIf</span></span>
<span data-ttu-id="79115-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79115-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79115-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79115-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79115-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79115-130">CommonParameters</span></span>
<span data-ttu-id="79115-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79115-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79115-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79115-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79115-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79115-133">INPUTS</span></span>

### <span data-ttu-id="79115-134">System. String</span><span class="sxs-lookup"><span data-stu-id="79115-134">System.String</span></span>

### <span data-ttu-id="79115-135">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="79115-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="79115-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79115-136">OUTPUTS</span></span>

### <span data-ttu-id="79115-137">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="79115-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="79115-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79115-138">NOTES</span></span>

## <span data-ttu-id="79115-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79115-139">RELATED LINKS</span></span>
