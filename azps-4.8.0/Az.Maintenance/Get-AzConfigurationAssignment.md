---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111655"
---
# <span data-ttu-id="a0c85-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a0c85-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="a0c85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0c85-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c85-103">Lista configurationAssignments para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c85-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="a0c85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0c85-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0c85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0c85-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c85-106">Lista configurationAssignments para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c85-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="a0c85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0c85-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c85-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0c85-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="a0c85-109">List configurationAssignments para host dedicado.</span><span class="sxs-lookup"><span data-stu-id="a0c85-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="a0c85-110">OS</span><span class="sxs-lookup"><span data-stu-id="a0c85-110">PARAMETERS</span></span>

### <span data-ttu-id="a0c85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c85-111">-DefaultProfile</span></span>
<span data-ttu-id="a0c85-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c85-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c85-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="a0c85-113">-ProviderName</span></span>
<span data-ttu-id="a0c85-114">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0c85-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="a0c85-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c85-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0c85-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0c85-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="a0c85-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a0c85-117">-ResourceName</span></span>
<span data-ttu-id="a0c85-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c85-118">The resource name.</span></span>

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

### <span data-ttu-id="a0c85-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="a0c85-119">-ResourceParentName</span></span>
<span data-ttu-id="a0c85-120">O nome do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="a0c85-120">The parent resource name.</span></span>

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

### <span data-ttu-id="a0c85-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="a0c85-121">-ResourceParentType</span></span>
<span data-ttu-id="a0c85-122">O tipo de recurso pai.</span><span class="sxs-lookup"><span data-stu-id="a0c85-122">The parent resource type.</span></span>

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

### <span data-ttu-id="a0c85-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a0c85-123">-ResourceType</span></span>
<span data-ttu-id="a0c85-124">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c85-124">The resource type.</span></span>

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

### <span data-ttu-id="a0c85-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c85-125">CommonParameters</span></span>
<span data-ttu-id="a0c85-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c85-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c85-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0c85-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c85-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0c85-128">INPUTS</span></span>

### <span data-ttu-id="a0c85-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a0c85-129">System.String</span></span>

## <span data-ttu-id="a0c85-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0c85-130">OUTPUTS</span></span>

### <span data-ttu-id="a0c85-131">Microsoft. Azure. Commands. maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="a0c85-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="a0c85-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0c85-132">NOTES</span></span>

## <span data-ttu-id="a0c85-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0c85-133">RELATED LINKS</span></span>
