---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428221"
---
# <span data-ttu-id="3b3b9-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="3b3b9-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="3b3b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b3b9-102">SYNOPSIS</span></span>

<span data-ttu-id="3b3b9-103">Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3b9-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b3b9-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="3b3b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b3b9-105">DESCRIPTION</span></span>

<span data-ttu-id="3b3b9-106">O cmdlet Sync-AzureAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3b3b9-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="3b3b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b3b9-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3b9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b3b9-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="3b3b9-109">Esse comando sincronizará o banco de dados chamado SalesOrders no servidor chamado ' contoso ' no ambiente westus.asazure.windows.net desde que o usuário tenha se conectado nesse ambiente usando Add-AzureAnalysisServicesAccount comando.</span><span class="sxs-lookup"><span data-stu-id="3b3b9-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="3b3b9-110">OS</span><span class="sxs-lookup"><span data-stu-id="3b3b9-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3b9-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="3b3b9-111">-Instance</span></span>

<span data-ttu-id="3b3b9-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="3b3b9-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b9-113">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="3b3b9-113">-Database</span></span>

<span data-ttu-id="3b3b9-114">Identidade do banco de dados a ser sincronizado</span><span class="sxs-lookup"><span data-stu-id="3b3b9-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3b9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b3b9-115">-PassThru</span></span>

<span data-ttu-id="3b3b9-116">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3b3b9-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3b3b9-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b3b9-117">INPUTS</span></span>

### <span data-ttu-id="3b3b9-118">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3b3b9-118">None</span></span>
<span data-ttu-id="3b3b9-119">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3b3b9-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b3b9-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b3b9-120">OUTPUTS</span></span>

### <span data-ttu-id="3b3b9-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b3b9-121">System.Boolean</span></span>

## <span data-ttu-id="3b3b9-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b3b9-122">NOTES</span></span>

<span data-ttu-id="3b3b9-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="3b3b9-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="3b3b9-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b3b9-124">RELATED LINKS</span></span>
