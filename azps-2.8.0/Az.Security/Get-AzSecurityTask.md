---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
ms.openlocfilehash: 9d1ce9dc517e550fdfada1db000657aedc15c6ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773262"
---
# <span data-ttu-id="eb6b8-101">Get-AzSecurityTask</span><span class="sxs-lookup"><span data-stu-id="eb6b8-101">Get-AzSecurityTask</span></span>

## <span data-ttu-id="eb6b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6b8-103">Obtém as tarefas de segurança que a central de segurança do Azure recomenda fazer para que você possa reforçar sua postura de segurança.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

## <span data-ttu-id="eb6b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb6b8-104">SYNTAX</span></span>

### <span data-ttu-id="eb6b8-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6b8-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="eb6b8-106">ResourceGroupScope</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6b8-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="eb6b8-107">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb6b8-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="eb6b8-108">SubscriptionLevelResource</span></span>
```
Get-AzSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6b8-109">Identificação</span><span class="sxs-lookup"><span data-stu-id="eb6b8-109">ResourceId</span></span>
```
Get-AzSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb6b8-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb6b8-110">DESCRIPTION</span></span>
<span data-ttu-id="eb6b8-111">A central de segurança do Azure verifica seus recursos para detectar possíveis problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="eb6b8-112">Esse cmdlet permite que você descubra as tarefas de segurança que a central de segurança do Azure recomenda que você faça.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="eb6b8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb6b8-113">EXAMPLES</span></span>

### <span data-ttu-id="eb6b8-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb6b8-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="eb6b8-115">Obtém todas as tarefas de segurança descobertas em recursos dentro de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="eb6b8-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb6b8-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="eb6b8-117">Obtém todas as tarefas de segurança descobertas em recursos dentro de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="eb6b8-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="eb6b8-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="eb6b8-119">Obtém uma tarefa de segurança específica.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-119">Gets a specific security task.</span></span>

## <span data-ttu-id="eb6b8-120">OS</span><span class="sxs-lookup"><span data-stu-id="eb6b8-120">PARAMETERS</span></span>

### <span data-ttu-id="eb6b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6b8-121">-DefaultProfile</span></span>
<span data-ttu-id="eb6b8-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb6b8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb6b8-123">-Name</span></span>
<span data-ttu-id="eb6b8-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb6b8-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb6b8-127">-ResourceId</span></span>
<span data-ttu-id="eb6b8-128">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb6b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6b8-129">CommonParameters</span></span>
<span data-ttu-id="eb6b8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6b8-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6b8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6b8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb6b8-132">INPUTS</span></span>

### <span data-ttu-id="eb6b8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6b8-133">System.String</span></span>

## <span data-ttu-id="eb6b8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb6b8-134">OUTPUTS</span></span>

### <span data-ttu-id="eb6b8-135">Microsoft. Azure. Commands. Security. Models. Tasks. PSSecurityTask</span><span class="sxs-lookup"><span data-stu-id="eb6b8-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="eb6b8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb6b8-136">NOTES</span></span>

## <span data-ttu-id="eb6b8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb6b8-137">RELATED LINKS</span></span>