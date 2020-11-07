---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 5353009c2001d043511e7e6af23fb7d4ccf84763
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775745"
---
# <span data-ttu-id="0b7b5-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0b7b5-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="0b7b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7b5-103">Obtém as categorias registradas e os refinamentos de tempo.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="0b7b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b7b5-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b7b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="0b7b5-106">O cmdlet **Get-AzDiagnosticSetting** Obtém as categorias e os refinamentos de tempo que são registrados para um recurso.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="0b7b5-107">Um intervalo de tempo é o intervalo de agregação de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="0b7b5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b7b5-108">EXAMPLES</span></span>

### <span data-ttu-id="0b7b5-109">Exemplo 1: obter o status das categorias de log e dos refinamentos de tempo</span><span class="sxs-lookup"><span data-stu-id="0b7b5-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="0b7b5-110">Esse comando obtém as categorias e os detalhamentos de tempo que são registrados para um cofre do Azure Key com uma *Resourceação* de/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="0b7b5-111">OS</span><span class="sxs-lookup"><span data-stu-id="0b7b5-111">PARAMETERS</span></span>

### <span data-ttu-id="0b7b5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7b5-112">-DefaultProfile</span></span>
<span data-ttu-id="0b7b5-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b7b5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b7b5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b7b5-114">-Name</span></span>
<span data-ttu-id="0b7b5-115">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="0b7b5-116">Se não tiver recebido a chamada padrão para "serviço" como estava na API anterior.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="0b7b5-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b7b5-117">-ResourceId</span></span>
<span data-ttu-id="0b7b5-118">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="0b7b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7b5-119">CommonParameters</span></span>
<span data-ttu-id="0b7b5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7b5-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b7b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7b5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b7b5-122">INPUTS</span></span>

### <span data-ttu-id="0b7b5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0b7b5-123">System.String</span></span>

## <span data-ttu-id="0b7b5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b7b5-124">OUTPUTS</span></span>

### <span data-ttu-id="0b7b5-125">Microsoft. Azure. Commands. insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="0b7b5-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="0b7b5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b7b5-126">NOTES</span></span>

## <span data-ttu-id="0b7b5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b7b5-127">RELATED LINKS</span></span>

<span data-ttu-id="0b7b5-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="0b7b5-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
