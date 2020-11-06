---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440650"
---
# <span data-ttu-id="219f0-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="219f0-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="219f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="219f0-102">SYNOPSIS</span></span>
<span data-ttu-id="219f0-103">Cria um novo trabalho de dispositivos de exportação.</span><span class="sxs-lookup"><span data-stu-id="219f0-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="219f0-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="219f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="219f0-105">DESCRIPTION</span></span>
<span data-ttu-id="219f0-106">Cria um novo trabalho de dispositivos de exportação para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="219f0-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="219f0-107">Esse procedimento exportará todos os dispositivos para o contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="219f0-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="219f0-108">Consulte o artigo a seguir sobre como gerar o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="219f0-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="219f0-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="219f0-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="219f0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="219f0-110">EXAMPLES</span></span>

### <span data-ttu-id="219f0-111">Exemplo 1 emita uma solicitação de exportação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="219f0-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="219f0-112">Cria uma nova solicitação de dispositivo de exportação para o IotHub "myiothub" excluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="219f0-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="219f0-113">OS</span><span class="sxs-lookup"><span data-stu-id="219f0-113">PARAMETERS</span></span>

### <span data-ttu-id="219f0-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="219f0-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="219f0-115">O URI para o qual exportar o blob.</span><span class="sxs-lookup"><span data-stu-id="219f0-115">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219f0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="219f0-116">-Name</span></span>
<span data-ttu-id="219f0-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="219f0-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="219f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="219f0-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="219f0-119">Resource Group Name</span></span>

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

### <span data-ttu-id="219f0-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="219f0-120">-Confirm</span></span>
<span data-ttu-id="219f0-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219f0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219f0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219f0-122">-WhatIf</span></span>
<span data-ttu-id="219f0-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="219f0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219f0-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="219f0-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219f0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219f0-125">-DefaultProfile</span></span>
<span data-ttu-id="219f0-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="219f0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="219f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219f0-127">CommonParameters</span></span>
<span data-ttu-id="219f0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219f0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219f0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="219f0-130">INPUTS</span></span>

### <span data-ttu-id="219f0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="219f0-131">System.String</span></span>

## <span data-ttu-id="219f0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="219f0-132">OUTPUTS</span></span>

### <span data-ttu-id="219f0-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="219f0-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="219f0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="219f0-134">NOTES</span></span>

## <span data-ttu-id="219f0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="219f0-135">RELATED LINKS</span></span>

