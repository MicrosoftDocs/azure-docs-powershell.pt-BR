---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610338"
---
# <span data-ttu-id="c1c2d-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="c1c2d-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="c1c2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c2d-103">Obtém as informações sobre um trabalho do IotHub.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1c2d-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c2d-106">Obtém as informações sobre um trabalho do IotHub.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="c1c2d-107">Um trabalho do IotHub é criado quando uma operação de importação ou exportação é initialted usando os comandos New-AzureRmIotHubExportDevices ou New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="c1c2d-108">Você pode fazer uma lista de todos os trabalhos ou filtrar os trabalhos pelo identificador do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="c1c2d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1c2d-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c2d-110">Exemplo 1 listar todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="c1c2d-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c1c2d-111">Obtém todos os trabalhos para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c1c2d-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="c1c2d-112">Exemplo 2 obter um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="c1c2d-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="c1c2d-113">Obtém informações sobre o trabalho com o identificador "3630fc31-4caa-43e8-A232-ea0577221cb2" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c1c2d-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c1c2d-114">OS</span><span class="sxs-lookup"><span data-stu-id="c1c2d-114">PARAMETERS</span></span>

### <span data-ttu-id="c1c2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c2d-115">-DefaultProfile</span></span>
<span data-ttu-id="c1c2d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c1c2d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c2d-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c1c2d-117">-JobId</span></span>
<span data-ttu-id="c1c2d-118">O identificador do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="c1c2d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1c2d-119">-Name</span></span>
<span data-ttu-id="c1c2d-120">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="c1c2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1c2d-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c1c2d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="c1c2d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c2d-123">CommonParameters</span></span>
<span data-ttu-id="c1c2d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c2d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c2d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c2d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c2d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1c2d-126">INPUTS</span></span>

### <span data-ttu-id="c1c2d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c2d-127">System.String</span></span>

## <span data-ttu-id="c1c2d-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1c2d-128">OUTPUTS</span></span>

### <span data-ttu-id="c1c2d-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="c1c2d-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="c1c2d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1c2d-130">NOTES</span></span>

## <span data-ttu-id="c1c2d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1c2d-131">RELATED LINKS</span></span>
