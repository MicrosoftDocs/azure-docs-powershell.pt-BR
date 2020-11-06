---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428017"
---
# <span data-ttu-id="9a522-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="9a522-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="9a522-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a522-102">SYNOPSIS</span></span>
<span data-ttu-id="9a522-103">Sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a522-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a522-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a522-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a522-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a522-105">DESCRIPTION</span></span>
<span data-ttu-id="9a522-106">O cmdlet Sync-AzureAnalysisServicesInstance sincroniza um banco de dados especificado na instância especificada do servidor do Analysis Services para todas as instâncias de dimensionamento de consulta no ambiente atualmente conectado, conforme especificado no comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9a522-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="9a522-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a522-107">EXAMPLES</span></span>

### <span data-ttu-id="9a522-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a522-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="9a522-109">Esse comando sincronizará o banco de dados chamado SalesOrders no servidor chamado ' contoso ' no ambiente westus.asazure.windows.net desde que o usuário tenha se conectado nesse ambiente usando Add-AzureAnalysisServicesAccount comando.</span><span class="sxs-lookup"><span data-stu-id="9a522-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="9a522-110">OS</span><span class="sxs-lookup"><span data-stu-id="9a522-110">PARAMETERS</span></span>

### <span data-ttu-id="9a522-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="9a522-111">-Instance</span></span>
<span data-ttu-id="9a522-112">Nome da instância do servidor do Analysis Services para reiniciar</span><span class="sxs-lookup"><span data-stu-id="9a522-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a522-113">-Banco de dados</span><span class="sxs-lookup"><span data-stu-id="9a522-113">-Database</span></span>
<span data-ttu-id="9a522-114">Identidade do banco de dados a ser sincronizado</span><span class="sxs-lookup"><span data-stu-id="9a522-114">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a522-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a522-115">-PassThru</span></span>
<span data-ttu-id="9a522-116">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9a522-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9a522-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a522-117">-Confirm</span></span>
<span data-ttu-id="9a522-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a522-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a522-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a522-119">-WhatIf</span></span>
<span data-ttu-id="9a522-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a522-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a522-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a522-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a522-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a522-122">CommonParameters</span></span>
<span data-ttu-id="9a522-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a522-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a522-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a522-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a522-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a522-125">INPUTS</span></span>

## <span data-ttu-id="9a522-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a522-126">OUTPUTS</span></span>

### <span data-ttu-id="9a522-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a522-127">System.Boolean</span></span>

## <span data-ttu-id="9a522-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a522-128">NOTES</span></span>
<span data-ttu-id="9a522-129">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="9a522-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="9a522-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a522-130">RELATED LINKS</span></span>

