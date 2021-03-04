---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 191b5a75a5f9f581308c8d5aa214fe4f2ae84851
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889948"
---
# <span data-ttu-id="034c7-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="034c7-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="034c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034c7-102">SYNOPSIS</span></span>
<span data-ttu-id="034c7-103">Obtém as informações sobre um trabalho IotHub.</span><span class="sxs-lookup"><span data-stu-id="034c7-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="034c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="034c7-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="034c7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="034c7-105">DESCRIPTION</span></span>
<span data-ttu-id="034c7-106">Obtém as informações sobre um trabalho IotHub.</span><span class="sxs-lookup"><span data-stu-id="034c7-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="034c7-107">Um trabalho IotHub é criado quando uma operação de importação ou exportação é inicializada usando os comandos New-AzIotHubExportDevices ou New-AzIotHubImportDevices de exportação.</span><span class="sxs-lookup"><span data-stu-id="034c7-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="034c7-108">Você pode listar todos os trabalhos ou filtrar os trabalhos pelo Identificador de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="034c7-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="034c7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="034c7-109">EXAMPLES</span></span>

### <span data-ttu-id="034c7-110">Exemplo 1 Listar todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="034c7-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="034c7-111">Obtém todos os trabalhos do IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="034c7-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="034c7-112">Exemplo 2 Obter um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="034c7-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="034c7-113">Obtém informações sobre o trabalho com o identificador "3630fc31-4caa-43e8-a232-ea057221cb2" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="034c7-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="034c7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="034c7-114">PARAMETERS</span></span>

### <span data-ttu-id="034c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034c7-115">-DefaultProfile</span></span>
<span data-ttu-id="034c7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="034c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034c7-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="034c7-117">-JobId</span></span>
<span data-ttu-id="034c7-118">O Identificador de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="034c7-118">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="034c7-119">-Name</span></span>
<span data-ttu-id="034c7-120">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="034c7-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="034c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="034c7-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="034c7-122">Resource Group Name</span></span>

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

### <span data-ttu-id="034c7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034c7-123">CommonParameters</span></span>
<span data-ttu-id="034c7-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034c7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034c7-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034c7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034c7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="034c7-126">INPUTS</span></span>

### <span data-ttu-id="034c7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="034c7-127">System.String</span></span>

## <span data-ttu-id="034c7-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="034c7-128">OUTPUTS</span></span>

### <span data-ttu-id="034c7-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="034c7-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="034c7-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="034c7-130">NOTES</span></span>

## <span data-ttu-id="034c7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="034c7-131">RELATED LINKS</span></span>
