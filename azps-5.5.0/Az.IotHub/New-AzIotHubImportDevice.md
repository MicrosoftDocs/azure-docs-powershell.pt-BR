---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111849"
---
# <span data-ttu-id="5d580-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="5d580-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="5d580-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d580-102">SYNOPSIS</span></span>
<span data-ttu-id="5d580-103">Cria um novo trabalho de importação de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5d580-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="5d580-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d580-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d580-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d580-105">DESCRIPTION</span></span>
<span data-ttu-id="5d580-106">Cria um novo trabalho de importação de dispositivos para o IotHub.</span><span class="sxs-lookup"><span data-stu-id="5d580-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="5d580-107">Isso importa todos os dispositivos para o IotHub do contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="5d580-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="5d580-108">Confira o seguinte artigo sobre como gerar o URI SAS.</span><span class="sxs-lookup"><span data-stu-id="5d580-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="5d580-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="5d580-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="5d580-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d580-110">EXAMPLES</span></span>

### <span data-ttu-id="5d580-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5d580-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="5d580-112">Cria uma nova solicitação de dispositivo de importação para o IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5d580-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="5d580-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d580-113">PARAMETERS</span></span>

### <span data-ttu-id="5d580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d580-114">-DefaultProfile</span></span>
<span data-ttu-id="5d580-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5d580-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d580-116">-InputBltContainerUri</span><span class="sxs-lookup"><span data-stu-id="5d580-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="5d580-117">Uri do Contêiner de Blob de Entrada para FileUpload</span><span class="sxs-lookup"><span data-stu-id="5d580-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="5d580-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d580-118">-Name</span></span>
<span data-ttu-id="5d580-119">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="5d580-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="5d580-120">-OutputBltContainerUri</span><span class="sxs-lookup"><span data-stu-id="5d580-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="5d580-121">O Uri para gravar a saída.</span><span class="sxs-lookup"><span data-stu-id="5d580-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d580-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d580-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d580-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5d580-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5d580-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5d580-124">-Confirm</span></span>
<span data-ttu-id="5d580-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d580-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d580-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d580-126">-WhatIf</span></span>
<span data-ttu-id="5d580-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5d580-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d580-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d580-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d580-129">CommonParameters</span></span>
<span data-ttu-id="5d580-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d580-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d580-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d580-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="5d580-132">INPUTS</span></span>

### <span data-ttu-id="5d580-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5d580-133">System.String</span></span>

## <span data-ttu-id="5d580-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="5d580-134">OUTPUTS</span></span>

### <span data-ttu-id="5d580-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="5d580-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="5d580-136">Notas</span><span class="sxs-lookup"><span data-stu-id="5d580-136">NOTES</span></span>

## <span data-ttu-id="5d580-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d580-137">RELATED LINKS</span></span>
