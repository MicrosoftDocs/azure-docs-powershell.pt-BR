---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609675"
---
# <span data-ttu-id="4de84-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4de84-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="4de84-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4de84-102">SYNOPSIS</span></span>
<span data-ttu-id="4de84-103">Obtém as categorias registradas e os refinamentos de tempo.</span><span class="sxs-lookup"><span data-stu-id="4de84-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4de84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4de84-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4de84-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4de84-105">DESCRIPTION</span></span>
<span data-ttu-id="4de84-106">O cmdlet **Get-AzureRmDiagnosticSetting** Obtém as categorias e os refinamentos de tempo que são registrados para um recurso.</span><span class="sxs-lookup"><span data-stu-id="4de84-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="4de84-107">Um intervalo de tempo é o intervalo de agregação de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="4de84-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="4de84-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4de84-108">EXAMPLES</span></span>

### <span data-ttu-id="4de84-109">Exemplo 1: obter o status das categorias de log e dos refinamentos de tempo</span><span class="sxs-lookup"><span data-stu-id="4de84-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="4de84-110">Esse comando obtém as categorias e os detalhamentos de tempo que são registrados para um cofre do Azure Key com uma *Resourceação* de/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4de84-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="4de84-111">OS</span><span class="sxs-lookup"><span data-stu-id="4de84-111">PARAMETERS</span></span>

### <span data-ttu-id="4de84-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4de84-112">-ResourceId</span></span>
<span data-ttu-id="4de84-113">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="4de84-113">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="4de84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de84-114">-DefaultProfile</span></span>
<span data-ttu-id="4de84-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4de84-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de84-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de84-116">CommonParameters</span></span>
<span data-ttu-id="4de84-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4de84-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de84-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4de84-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de84-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4de84-119">INPUTS</span></span>

## <span data-ttu-id="4de84-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4de84-120">OUTPUTS</span></span>

### <span data-ttu-id="4de84-121">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="4de84-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="4de84-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4de84-122">NOTES</span></span>

## <span data-ttu-id="4de84-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4de84-123">RELATED LINKS</span></span>

[<span data-ttu-id="4de84-124">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4de84-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


