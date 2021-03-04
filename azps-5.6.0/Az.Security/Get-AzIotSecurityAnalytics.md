---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: aaa7e89334f2736010e4a762012d5c456a0fac4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887630"
---
# <span data-ttu-id="ddf75-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="ddf75-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="ddf75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf75-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf75-103">Obter análise de segurança da IoT</span><span class="sxs-lookup"><span data-stu-id="ddf75-103">Get IoT security analytics</span></span>

## <span data-ttu-id="ddf75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ddf75-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf75-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ddf75-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf75-106">O Get-AzIotSecurityAnalytics cmdlet retorna um conjunto de análises de segurança de uma solução de segurança iot específica</span><span class="sxs-lookup"><span data-stu-id="ddf75-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="ddf75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddf75-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddf75-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="ddf75-109">Obter a Análise de Segurança de IoT para Solução de Segurança "MySolution" em reasource group "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="ddf75-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="ddf75-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ddf75-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf75-111">-Default</span><span class="sxs-lookup"><span data-stu-id="ddf75-111">-Default</span></span>
<span data-ttu-id="ddf75-112">Se presente, obter o conjunto de análises padrão, caso contrário, obter a lista de todos os conjuntos de análise.</span><span class="sxs-lookup"><span data-stu-id="ddf75-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf75-113">-DefaultProfile</span></span>
<span data-ttu-id="ddf75-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf75-115">-ResourceGroupName</span></span>
<span data-ttu-id="ddf75-116">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddf75-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf75-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="ddf75-117">-SolutionName</span></span>
<span data-ttu-id="ddf75-118">Nome da solução</span><span class="sxs-lookup"><span data-stu-id="ddf75-118">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf75-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf75-119">CommonParameters</span></span>
<span data-ttu-id="ddf75-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf75-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf75-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddf75-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf75-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddf75-122">INPUTS</span></span>

### <span data-ttu-id="ddf75-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ddf75-123">None</span></span>

## <span data-ttu-id="ddf75-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ddf75-124">OUTPUTS</span></span>

### <span data-ttu-id="ddf75-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="ddf75-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="ddf75-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="ddf75-126">NOTES</span></span>

## <span data-ttu-id="ddf75-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddf75-127">RELATED LINKS</span></span>
