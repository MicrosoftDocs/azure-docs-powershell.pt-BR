---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610393"
---
# <span data-ttu-id="33f17-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="33f17-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="33f17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33f17-102">SYNOPSIS</span></span>
<span data-ttu-id="33f17-103">Cria um novo trabalho de dispositivos de exportação.</span><span class="sxs-lookup"><span data-stu-id="33f17-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33f17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33f17-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33f17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33f17-105">DESCRIPTION</span></span>
<span data-ttu-id="33f17-106">Cria um novo trabalho de dispositivos de exportação para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="33f17-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="33f17-107">Esse procedimento exportará todos os dispositivos para o contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="33f17-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="33f17-108">Consulte o artigo a seguir sobre como gerar o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="33f17-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="33f17-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="33f17-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="33f17-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33f17-110">EXAMPLES</span></span>

### <span data-ttu-id="33f17-111">Exemplo 1 emita uma solicitação de exportação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="33f17-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="33f17-112">Cria uma nova solicitação de dispositivo de exportação para o IotHub "myiothub" excluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="33f17-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="33f17-113">OS</span><span class="sxs-lookup"><span data-stu-id="33f17-113">PARAMETERS</span></span>

### <span data-ttu-id="33f17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f17-114">-DefaultProfile</span></span>
<span data-ttu-id="33f17-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="33f17-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33f17-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="33f17-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="33f17-117">O URI para o qual exportar o blob.</span><span class="sxs-lookup"><span data-stu-id="33f17-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f17-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="33f17-118">-Name</span></span>
<span data-ttu-id="33f17-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="33f17-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="33f17-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f17-120">-ResourceGroupName</span></span>
<span data-ttu-id="33f17-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="33f17-121">Resource Group Name</span></span>

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

### <span data-ttu-id="33f17-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33f17-122">-Confirm</span></span>
<span data-ttu-id="33f17-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33f17-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f17-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33f17-124">-WhatIf</span></span>
<span data-ttu-id="33f17-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33f17-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33f17-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33f17-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33f17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f17-127">CommonParameters</span></span>
<span data-ttu-id="33f17-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f17-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33f17-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f17-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33f17-130">INPUTS</span></span>

### <span data-ttu-id="33f17-131">System. String</span><span class="sxs-lookup"><span data-stu-id="33f17-131">System.String</span></span>

## <span data-ttu-id="33f17-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33f17-132">OUTPUTS</span></span>

### <span data-ttu-id="33f17-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="33f17-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="33f17-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33f17-134">NOTES</span></span>

## <span data-ttu-id="33f17-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33f17-135">RELATED LINKS</span></span>

