---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 84b8224c83e6455e7f59b8a5fe2b330f34e61ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429770"
---
# <span data-ttu-id="ee709-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="ee709-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="ee709-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee709-102">SYNOPSIS</span></span>
<span data-ttu-id="ee709-103">Cria um novo trabalho de dispositivos de importação.</span><span class="sxs-lookup"><span data-stu-id="ee709-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee709-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee709-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee709-105">DESCRIPTION</span></span>
<span data-ttu-id="ee709-106">Cria um novo trabalho de dispositivos de importação para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="ee709-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="ee709-107">Isso importará todos os dispositivos para o IotHub a partir do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="ee709-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="ee709-108">Consulte o artigo a seguir sobre como gerar o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="ee709-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="ee709-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="ee709-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="ee709-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee709-110">EXAMPLES</span></span>

### <span data-ttu-id="ee709-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ee709-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="ee709-112">Cria uma nova solicitação de dispositivo de importação para o IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ee709-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="ee709-113">OS</span><span class="sxs-lookup"><span data-stu-id="ee709-113">PARAMETERS</span></span>

### <span data-ttu-id="ee709-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee709-114">-DefaultProfile</span></span>
<span data-ttu-id="ee709-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ee709-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee709-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="ee709-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="ee709-117">URI do contêiner de blob de entrada para FileUpload</span><span class="sxs-lookup"><span data-stu-id="ee709-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="ee709-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee709-118">-Name</span></span>
<span data-ttu-id="ee709-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="ee709-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="ee709-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="ee709-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="ee709-121">O URI no qual a saída será gravada.</span><span class="sxs-lookup"><span data-stu-id="ee709-121">The Uri to write the output to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee709-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee709-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee709-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ee709-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ee709-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee709-124">-Confirm</span></span>
<span data-ttu-id="ee709-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee709-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee709-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee709-126">-WhatIf</span></span>
<span data-ttu-id="ee709-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee709-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee709-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee709-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee709-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee709-129">CommonParameters</span></span>
<span data-ttu-id="ee709-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee709-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee709-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee709-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee709-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee709-132">INPUTS</span></span>

### <span data-ttu-id="ee709-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ee709-133">System.String</span></span>

## <span data-ttu-id="ee709-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee709-134">OUTPUTS</span></span>

### <span data-ttu-id="ee709-135">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="ee709-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="ee709-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee709-136">NOTES</span></span>

## <span data-ttu-id="ee709-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee709-137">RELATED LINKS</span></span>

