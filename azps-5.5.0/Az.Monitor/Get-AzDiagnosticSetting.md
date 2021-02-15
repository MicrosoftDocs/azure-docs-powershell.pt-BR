---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111763"
---
# <span data-ttu-id="724c1-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="724c1-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="724c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="724c1-102">SYNOPSIS</span></span>
<span data-ttu-id="724c1-103">Obtém as categorias registradas e os prazos.</span><span class="sxs-lookup"><span data-stu-id="724c1-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="724c1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="724c1-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="724c1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="724c1-105">DESCRIPTION</span></span>
<span data-ttu-id="724c1-106">O cmdlet **Get-AzDiagnosticSetting** obtém as categorias e os tempos que são registrados para um recurso.</span><span class="sxs-lookup"><span data-stu-id="724c1-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="724c1-107">Um intervalo de tempo é o intervalo de agregação de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="724c1-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="724c1-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="724c1-108">EXAMPLES</span></span>

### <span data-ttu-id="724c1-109">Exemplo 1: Obter o status das categorias de registro em log e de tempo</span><span class="sxs-lookup"><span data-stu-id="724c1-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="724c1-110">Esse comando obtém as categorias e os tempos que são registrados em um Cofre de Chaves do Azure com uma *ResourceId* de /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="724c1-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="724c1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="724c1-111">PARAMETERS</span></span>

### <span data-ttu-id="724c1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724c1-112">-DefaultProfile</span></span>
<span data-ttu-id="724c1-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="724c1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="724c1-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="724c1-114">-Name</span></span>
<span data-ttu-id="724c1-115">O nome da configuração de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="724c1-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="724c1-116">Se não tiver dado o padrão de chamada para "serviço", como estava na API anterior.</span><span class="sxs-lookup"><span data-stu-id="724c1-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="724c1-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="724c1-117">-ResourceId</span></span>
<span data-ttu-id="724c1-118">Especifica a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="724c1-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="724c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724c1-119">CommonParameters</span></span>
<span data-ttu-id="724c1-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724c1-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="724c1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724c1-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="724c1-122">INPUTS</span></span>

### <span data-ttu-id="724c1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="724c1-123">System.String</span></span>

## <span data-ttu-id="724c1-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="724c1-124">OUTPUTS</span></span>

### <span data-ttu-id="724c1-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="724c1-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="724c1-126">Notas</span><span class="sxs-lookup"><span data-stu-id="724c1-126">NOTES</span></span>

## <span data-ttu-id="724c1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="724c1-127">RELATED LINKS</span></span>

<span data-ttu-id="724c1-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="724c1-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
