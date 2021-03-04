---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888894"
---
# <span data-ttu-id="22feb-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="22feb-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="22feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22feb-102">SYNOPSIS</span></span>
<span data-ttu-id="22feb-103">Obtém as categorias registradas e os grãos de tempo.</span><span class="sxs-lookup"><span data-stu-id="22feb-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="22feb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="22feb-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22feb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="22feb-105">DESCRIPTION</span></span>
<span data-ttu-id="22feb-106">O cmdlet **Get-AzDiagnosticSetting** obtém as categorias e os grãos de tempo registrados para um recurso.</span><span class="sxs-lookup"><span data-stu-id="22feb-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="22feb-107">Um grain de tempo é o intervalo de agregação de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="22feb-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="22feb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22feb-108">EXAMPLES</span></span>

### <span data-ttu-id="22feb-109">Exemplo 1: Obter o status das categorias de registro em log e dos grãos de tempo</span><span class="sxs-lookup"><span data-stu-id="22feb-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="22feb-110">Este comando obtém as categorias e os grãos de tempo registrados para um Cofre de Chaves do Azure com *um ResourceId* de /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="22feb-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="22feb-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="22feb-111">PARAMETERS</span></span>

### <span data-ttu-id="22feb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22feb-112">-DefaultProfile</span></span>
<span data-ttu-id="22feb-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="22feb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22feb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="22feb-114">-Name</span></span>
<span data-ttu-id="22feb-115">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="22feb-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="22feb-116">Se não for dado o padrão de chamada para "serviço" como estava na API anterior.</span><span class="sxs-lookup"><span data-stu-id="22feb-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="22feb-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22feb-117">-ResourceId</span></span>
<span data-ttu-id="22feb-118">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="22feb-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="22feb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22feb-119">CommonParameters</span></span>
<span data-ttu-id="22feb-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22feb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22feb-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22feb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22feb-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22feb-122">INPUTS</span></span>

### <span data-ttu-id="22feb-123">System.String</span><span class="sxs-lookup"><span data-stu-id="22feb-123">System.String</span></span>

## <span data-ttu-id="22feb-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="22feb-124">OUTPUTS</span></span>

### <span data-ttu-id="22feb-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="22feb-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="22feb-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="22feb-126">NOTES</span></span>

## <span data-ttu-id="22feb-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22feb-127">RELATED LINKS</span></span>

<span data-ttu-id="22feb-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="22feb-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
