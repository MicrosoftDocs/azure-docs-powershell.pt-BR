---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 36371899f1ac8c20bedf8a97bbf262d4df05fa12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773187"
---
# <span data-ttu-id="d2f98-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="d2f98-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="d2f98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2f98-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f98-103">Adicione ou atualize uma ou várias configurações do Service Fabric para o cluster.</span><span class="sxs-lookup"><span data-stu-id="d2f98-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="d2f98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2f98-104">SYNTAX</span></span>

### <span data-ttu-id="d2f98-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="d2f98-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f98-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="d2f98-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f98-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2f98-107">DESCRIPTION</span></span>
<span data-ttu-id="d2f98-108">Use **set-AzServiceFabricSetting** para adicionar ou atualizar as configurações do Service Fabric em um cluster.</span><span class="sxs-lookup"><span data-stu-id="d2f98-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="d2f98-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2f98-109">EXAMPLES</span></span>

### <span data-ttu-id="d2f98-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2f98-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="d2f98-111">Esse comando definirá ' MaxFileOperationTimeout ' como o valor ' 5000 ' na seção ' NamingService '.</span><span class="sxs-lookup"><span data-stu-id="d2f98-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="d2f98-112">OS</span><span class="sxs-lookup"><span data-stu-id="d2f98-112">PARAMETERS</span></span>

### <span data-ttu-id="d2f98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f98-113">-DefaultProfile</span></span>
<span data-ttu-id="d2f98-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f98-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2f98-115">-Name</span></span>
<span data-ttu-id="d2f98-116">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="d2f98-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="d2f98-117">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2f98-117">-Parameter</span></span>
<span data-ttu-id="d2f98-118">Nome do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="d2f98-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="d2f98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f98-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2f98-120">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2f98-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d2f98-121">-Seção</span><span class="sxs-lookup"><span data-stu-id="d2f98-121">-Section</span></span>
<span data-ttu-id="d2f98-122">Nome da seção da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="d2f98-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="d2f98-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="d2f98-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="d2f98-124">Uma matriz de configurações da malha</span><span class="sxs-lookup"><span data-stu-id="d2f98-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="d2f98-125">-Valor</span><span class="sxs-lookup"><span data-stu-id="d2f98-125">-Value</span></span>
<span data-ttu-id="d2f98-126">Valor do parâmetro da configuração de malha</span><span class="sxs-lookup"><span data-stu-id="d2f98-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="d2f98-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2f98-127">-Confirm</span></span>
<span data-ttu-id="d2f98-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f98-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f98-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f98-129">-WhatIf</span></span>
<span data-ttu-id="d2f98-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2f98-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f98-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2f98-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f98-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f98-132">CommonParameters</span></span>
<span data-ttu-id="d2f98-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f98-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f98-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f98-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f98-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2f98-135">INPUTS</span></span>

### <span data-ttu-id="d2f98-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d2f98-136">System.String</span></span>

### <span data-ttu-id="d2f98-137">Microsoft. Azure. Commands. imfabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="d2f98-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="d2f98-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2f98-138">OUTPUTS</span></span>

### <span data-ttu-id="d2f98-139">Microsoft. Azure. Commands. imfabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d2f98-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d2f98-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2f98-140">NOTES</span></span>

## <span data-ttu-id="d2f98-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2f98-141">RELATED LINKS</span></span>