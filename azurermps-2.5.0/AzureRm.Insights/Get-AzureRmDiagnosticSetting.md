---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: eb7dbdee5d1d3d1574be30c5168d97dfcee6ab27
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785257"
---
# <span data-ttu-id="a7948-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a7948-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="a7948-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7948-102">SYNOPSIS</span></span>
<span data-ttu-id="a7948-103">Obtém as categorias registradas e os refinamentos de tempo.</span><span class="sxs-lookup"><span data-stu-id="a7948-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7948-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7948-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7948-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7948-105">DESCRIPTION</span></span>
<span data-ttu-id="a7948-106">O cmdlet **Get-AzureRmDiagnosticSetting** Obtém as categorias e os refinamentos de tempo que são registrados para um recurso.</span><span class="sxs-lookup"><span data-stu-id="a7948-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="a7948-107">Um intervalo de tempo é o intervalo de agregação de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="a7948-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="a7948-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7948-108">EXAMPLES</span></span>

### <span data-ttu-id="a7948-109">Exemplo 1: obter o status das categorias de log e dos refinamentos de tempo</span><span class="sxs-lookup"><span data-stu-id="a7948-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="a7948-110">Esse comando obtém as categorias e os detalhamentos de tempo que são registrados para um cofre do Azure Key com uma *Resourceação* de/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a7948-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="a7948-111">OS</span><span class="sxs-lookup"><span data-stu-id="a7948-111">PARAMETERS</span></span>

### <span data-ttu-id="a7948-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7948-112">-DefaultProfile</span></span>
<span data-ttu-id="a7948-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a7948-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7948-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7948-114">-Name</span></span>
<span data-ttu-id="a7948-115">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a7948-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="a7948-116">Se não tiver recebido a chamada padrão para "serviço" como estava na API anterior.</span><span class="sxs-lookup"><span data-stu-id="a7948-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="a7948-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7948-117">-ResourceId</span></span>
<span data-ttu-id="a7948-118">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7948-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="a7948-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7948-119">CommonParameters</span></span>
<span data-ttu-id="a7948-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7948-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7948-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7948-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7948-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7948-122">INPUTS</span></span>

### <span data-ttu-id="a7948-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a7948-123">System.String</span></span>

## <span data-ttu-id="a7948-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7948-124">OUTPUTS</span></span>

### <span data-ttu-id="a7948-125">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="a7948-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="a7948-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7948-126">NOTES</span></span>

## <span data-ttu-id="a7948-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7948-127">RELATED LINKS</span></span>

<span data-ttu-id="a7948-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="a7948-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
