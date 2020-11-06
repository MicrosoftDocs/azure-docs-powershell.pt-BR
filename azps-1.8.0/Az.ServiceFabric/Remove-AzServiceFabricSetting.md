---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 22cc09a405d124ef4bf44342077b53dc64f974b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599105"
---
# <span data-ttu-id="52ed7-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="52ed7-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="52ed7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="52ed7-103">Remova uma ou várias configurações da malha de serviço do cluster.</span><span class="sxs-lookup"><span data-stu-id="52ed7-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="52ed7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52ed7-104">SYNTAX</span></span>

### <span data-ttu-id="52ed7-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="52ed7-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ed7-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="52ed7-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ed7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="52ed7-108">Use **Remove-AzServiceFabricSetting** para remover as configurações do Service Fabric do cluster.</span><span class="sxs-lookup"><span data-stu-id="52ed7-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="52ed7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52ed7-109">EXAMPLES</span></span>

### <span data-ttu-id="52ed7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52ed7-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="52ed7-111">Este comando removerá as configurações ' MaxCursors ' na seção ' EseStore '.</span><span class="sxs-lookup"><span data-stu-id="52ed7-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="52ed7-112">OS</span><span class="sxs-lookup"><span data-stu-id="52ed7-112">PARAMETERS</span></span>

### <span data-ttu-id="52ed7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ed7-113">-DefaultProfile</span></span>
<span data-ttu-id="52ed7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52ed7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ed7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="52ed7-115">-Name</span></span>
<span data-ttu-id="52ed7-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="52ed7-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="52ed7-117">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="52ed7-117">-Parameter</span></span>
<span data-ttu-id="52ed7-118">Com.</span><span class="sxs-lookup"><span data-stu-id="52ed7-118">Parameter.</span></span>

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

### <span data-ttu-id="52ed7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ed7-119">-ResourceGroupName</span></span>
<span data-ttu-id="52ed7-120">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52ed7-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="52ed7-121">-Seção</span><span class="sxs-lookup"><span data-stu-id="52ed7-121">-Section</span></span>
<span data-ttu-id="52ed7-122">Seção.</span><span class="sxs-lookup"><span data-stu-id="52ed7-122">Section.</span></span>

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

### <span data-ttu-id="52ed7-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="52ed7-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="52ed7-124">Tipo de autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="52ed7-124">Client authentication type.</span></span>

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

### <span data-ttu-id="52ed7-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52ed7-125">-Confirm</span></span>
<span data-ttu-id="52ed7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ed7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ed7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ed7-127">-WhatIf</span></span>
<span data-ttu-id="52ed7-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52ed7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52ed7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52ed7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ed7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ed7-130">CommonParameters</span></span>
<span data-ttu-id="52ed7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ed7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ed7-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ed7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ed7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52ed7-133">INPUTS</span></span>

### <span data-ttu-id="52ed7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="52ed7-134">System.String</span></span>

### <span data-ttu-id="52ed7-135">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="52ed7-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="52ed7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52ed7-136">OUTPUTS</span></span>

### <span data-ttu-id="52ed7-137">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="52ed7-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="52ed7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52ed7-138">NOTES</span></span>

## <span data-ttu-id="52ed7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52ed7-139">RELATED LINKS</span></span>
