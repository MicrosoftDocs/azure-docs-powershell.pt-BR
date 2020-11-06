---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 4c13a6366f0ccae803e8020f16bf2b566bd70934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430919"
---
# <span data-ttu-id="1349e-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="1349e-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="1349e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1349e-102">SYNOPSIS</span></span>
<span data-ttu-id="1349e-103">Cria um novo trabalho de dispositivos de exportação.</span><span class="sxs-lookup"><span data-stu-id="1349e-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1349e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1349e-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1349e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1349e-105">DESCRIPTION</span></span>
<span data-ttu-id="1349e-106">Cria um novo trabalho de dispositivos de exportação para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="1349e-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="1349e-107">Esse procedimento exportará todos os dispositivos para o contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="1349e-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="1349e-108">Consulte o artigo a seguir sobre como gerar o URI da SAS.</span><span class="sxs-lookup"><span data-stu-id="1349e-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="1349e-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="1349e-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="1349e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1349e-110">EXAMPLES</span></span>

### <span data-ttu-id="1349e-111">Exemplo 1 emita uma solicitação de exportação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1349e-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="1349e-112">Cria uma nova solicitação de dispositivo de exportação para o IotHub "myiothub" excluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="1349e-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="1349e-113">OS</span><span class="sxs-lookup"><span data-stu-id="1349e-113">PARAMETERS</span></span>

### <span data-ttu-id="1349e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1349e-114">-DefaultProfile</span></span>
<span data-ttu-id="1349e-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1349e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1349e-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="1349e-116">-ExcludeKeys</span></span>
<span data-ttu-id="1349e-117">Permite exportar dispositivos sem chaves.</span><span class="sxs-lookup"><span data-stu-id="1349e-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="1349e-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1349e-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="1349e-119">O URI para o qual exportar o blob.</span><span class="sxs-lookup"><span data-stu-id="1349e-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="1349e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1349e-120">-Name</span></span>
<span data-ttu-id="1349e-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="1349e-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="1349e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1349e-122">-ResourceGroupName</span></span>
<span data-ttu-id="1349e-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1349e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1349e-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1349e-124">-Confirm</span></span>
<span data-ttu-id="1349e-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1349e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1349e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1349e-126">-WhatIf</span></span>
<span data-ttu-id="1349e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1349e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1349e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1349e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1349e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1349e-129">CommonParameters</span></span>
<span data-ttu-id="1349e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1349e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1349e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1349e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1349e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1349e-132">INPUTS</span></span>

### <span data-ttu-id="1349e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1349e-133">System.String</span></span>

## <span data-ttu-id="1349e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1349e-134">OUTPUTS</span></span>

### <span data-ttu-id="1349e-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="1349e-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="1349e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1349e-136">NOTES</span></span>

## <span data-ttu-id="1349e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1349e-137">RELATED LINKS</span></span>
