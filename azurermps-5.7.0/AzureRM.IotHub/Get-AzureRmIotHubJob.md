---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430462"
---
# <span data-ttu-id="4f495-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="4f495-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="4f495-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f495-102">SYNOPSIS</span></span>
<span data-ttu-id="4f495-103">Obtém as informações sobre um trabalho do IotHub.</span><span class="sxs-lookup"><span data-stu-id="4f495-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f495-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f495-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f495-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f495-105">DESCRIPTION</span></span>
<span data-ttu-id="4f495-106">Obtém as informações sobre um trabalho do IotHub.</span><span class="sxs-lookup"><span data-stu-id="4f495-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="4f495-107">Um trabalho do IotHub é criado quando uma operação de importação ou exportação é initialted usando os comandos New-AzureRmIotHubExportDevices ou New-AzureRmIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="4f495-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="4f495-108">Você pode fazer uma lista de todos os trabalhos ou filtrar os trabalhos pelo identificador do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4f495-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="4f495-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f495-109">EXAMPLES</span></span>

### <span data-ttu-id="4f495-110">Exemplo 1 listar todos os trabalhos</span><span class="sxs-lookup"><span data-stu-id="4f495-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4f495-111">Obtém todos os trabalhos para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4f495-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="4f495-112">Exemplo 2 obter um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="4f495-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="4f495-113">Obtém informações sobre o trabalho com o identificador "3630fc31-4caa-43e8-A232-ea0577221cb2" para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4f495-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4f495-114">OS</span><span class="sxs-lookup"><span data-stu-id="4f495-114">PARAMETERS</span></span>

### <span data-ttu-id="4f495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f495-115">-DefaultProfile</span></span>
<span data-ttu-id="4f495-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f495-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f495-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="4f495-117">-JobId</span></span>
<span data-ttu-id="4f495-118">O identificador do trabalho.</span><span class="sxs-lookup"><span data-stu-id="4f495-118">The Job Identifier.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f495-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f495-119">-Name</span></span>
<span data-ttu-id="4f495-120">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4f495-120">Name of the IoT hub.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f495-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f495-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f495-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4f495-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f495-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f495-123">CommonParameters</span></span>
<span data-ttu-id="4f495-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f495-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f495-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f495-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f495-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f495-126">INPUTS</span></span>

### <span data-ttu-id="4f495-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4f495-127">System.String</span></span>

## <span data-ttu-id="4f495-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f495-128">OUTPUTS</span></span>

### <span data-ttu-id="4f495-129">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="4f495-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="4f495-130">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="4f495-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="4f495-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f495-131">NOTES</span></span>

## <span data-ttu-id="4f495-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f495-132">RELATED LINKS</span></span>

