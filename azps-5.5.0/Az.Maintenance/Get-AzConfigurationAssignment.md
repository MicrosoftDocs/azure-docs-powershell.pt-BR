---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118444"
---
# <span data-ttu-id="b92b5-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b92b5-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="b92b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b92b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b92b5-103">Configuração de listaAssignments do recurso.</span><span class="sxs-lookup"><span data-stu-id="b92b5-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b92b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b92b5-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b92b5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b92b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b92b5-106">Configuração de listaAssignments do recurso.</span><span class="sxs-lookup"><span data-stu-id="b92b5-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b92b5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b92b5-107">EXAMPLES</span></span>

### <span data-ttu-id="b92b5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b92b5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="b92b5-109">Configuração de listaAssignments para host dedicado.</span><span class="sxs-lookup"><span data-stu-id="b92b5-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="b92b5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b92b5-110">PARAMETERS</span></span>

### <span data-ttu-id="b92b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92b5-111">-DefaultProfile</span></span>
<span data-ttu-id="b92b5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b92b5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b92b5-113">-Nomedo Provedor</span><span class="sxs-lookup"><span data-stu-id="b92b5-113">-ProviderName</span></span>
<span data-ttu-id="b92b5-114">Nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="b92b5-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b92b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="b92b5-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b92b5-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="b92b5-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b92b5-117">-ResourceName</span></span>
<span data-ttu-id="b92b5-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b92b5-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b92b5-119">-ResourceParentName</span></span>
<span data-ttu-id="b92b5-120">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b92b5-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b92b5-121">-ResourceParentType</span></span>
<span data-ttu-id="b92b5-122">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b92b5-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b92b5-123">-ResourceType</span></span>
<span data-ttu-id="b92b5-124">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b92b5-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92b5-125">CommonParameters</span></span>
<span data-ttu-id="b92b5-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92b5-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b92b5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92b5-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="b92b5-128">INPUTS</span></span>

### <span data-ttu-id="b92b5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b92b5-129">System.String</span></span>

## <span data-ttu-id="b92b5-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b92b5-130">OUTPUTS</span></span>

### <span data-ttu-id="b92b5-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b92b5-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="b92b5-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b92b5-132">NOTES</span></span>

## <span data-ttu-id="b92b5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b92b5-133">RELATED LINKS</span></span>
