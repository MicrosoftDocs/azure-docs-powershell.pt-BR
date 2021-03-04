---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 030c97a05d7f87ffc75c284250e8b67e8d3dc1fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885711"
---
# <span data-ttu-id="96ccb-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="96ccb-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="96ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="96ccb-103">Cria um novo trabalho de dispositivos de exportação.</span><span class="sxs-lookup"><span data-stu-id="96ccb-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="96ccb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96ccb-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96ccb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="96ccb-106">Cria um novo trabalho de dispositivos de exportação para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="96ccb-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="96ccb-107">Isso exportará todos os dispositivos para o contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="96ccb-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="96ccb-108">Consulte o artigo a seguir sobre como gerar o URI do SAS.</span><span class="sxs-lookup"><span data-stu-id="96ccb-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="96ccb-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="96ccb-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="96ccb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96ccb-110">EXAMPLES</span></span>

### <span data-ttu-id="96ccb-111">Exemplo 1 Emitir uma solicitação de dispositivo de exportação.</span><span class="sxs-lookup"><span data-stu-id="96ccb-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="96ccb-112">Cria uma nova solicitação de dispositivo de exportação para o IotHub "myiothub" excluindo as chaves.</span><span class="sxs-lookup"><span data-stu-id="96ccb-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="96ccb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96ccb-113">PARAMETERS</span></span>

### <span data-ttu-id="96ccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ccb-114">-DefaultProfile</span></span>
<span data-ttu-id="96ccb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="96ccb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96ccb-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="96ccb-116">-ExcludeKeys</span></span>
<span data-ttu-id="96ccb-117">Permite exportar dispositivos sem chaves.</span><span class="sxs-lookup"><span data-stu-id="96ccb-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="96ccb-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="96ccb-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="96ccb-119">O Uri para o que exportar o blob.</span><span class="sxs-lookup"><span data-stu-id="96ccb-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="96ccb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="96ccb-120">-Name</span></span>
<span data-ttu-id="96ccb-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="96ccb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="96ccb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ccb-122">-ResourceGroupName</span></span>
<span data-ttu-id="96ccb-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="96ccb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="96ccb-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96ccb-124">-Confirm</span></span>
<span data-ttu-id="96ccb-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96ccb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96ccb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96ccb-126">-WhatIf</span></span>
<span data-ttu-id="96ccb-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96ccb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96ccb-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96ccb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96ccb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ccb-129">CommonParameters</span></span>
<span data-ttu-id="96ccb-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96ccb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ccb-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96ccb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ccb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96ccb-132">INPUTS</span></span>

### <span data-ttu-id="96ccb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="96ccb-133">System.String</span></span>

## <span data-ttu-id="96ccb-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96ccb-134">OUTPUTS</span></span>

### <span data-ttu-id="96ccb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="96ccb-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="96ccb-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="96ccb-136">NOTES</span></span>

## <span data-ttu-id="96ccb-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96ccb-137">RELATED LINKS</span></span>
