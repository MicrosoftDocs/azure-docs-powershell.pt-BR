---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426809"
---
# <span data-ttu-id="218b6-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="218b6-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="218b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="218b6-102">SYNOPSIS</span></span>
<span data-ttu-id="218b6-103">Adiciona um ouvinte WinRM ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="218b6-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="218b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="218b6-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="218b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="218b6-105">DESCRIPTION</span></span>
<span data-ttu-id="218b6-106">O cmdlet **Add-AzureRmVmssWinRMListener** adiciona um ouvinte do Windows Remote Management (WinRM) no conjunto de escala da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="218b6-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="218b6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="218b6-107">EXAMPLES</span></span>

### <span data-ttu-id="218b6-108">Exemplo 1: adicionar um ouvinte do WinRM ao VMSS</span><span class="sxs-lookup"><span data-stu-id="218b6-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="218b6-109">Este exemplo adiciona um ouvinte do WinRM ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="218b6-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="218b6-110">O primeiro comando usa o cmdlet **New-AzureRmVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="218b6-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="218b6-111">O segundo comando adiciona um ouvinte de protocolo HTTP WinRM com o certificado na URL especificada para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="218b6-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="218b6-112">OS</span><span class="sxs-lookup"><span data-stu-id="218b6-112">PARAMETERS</span></span>

### <span data-ttu-id="218b6-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="218b6-113">-CertificateUrl</span></span>
<span data-ttu-id="218b6-114">Especifica um link, como uma URL, do certificado com o qual novas máquinas virtuais são provisionadas.</span><span class="sxs-lookup"><span data-stu-id="218b6-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218b6-115">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="218b6-115">-Protocol</span></span>
<span data-ttu-id="218b6-116">Especifica o protocolo do ouvinte de WinRM.</span><span class="sxs-lookup"><span data-stu-id="218b6-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="218b6-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="218b6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="218b6-118">Http</span><span class="sxs-lookup"><span data-stu-id="218b6-118">Http</span></span>
- <span data-ttu-id="218b6-119">Https</span><span class="sxs-lookup"><span data-stu-id="218b6-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218b6-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="218b6-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="218b6-121">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="218b6-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="218b6-122">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="218b6-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="218b6-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="218b6-123">-Confirm</span></span>
<span data-ttu-id="218b6-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="218b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218b6-125">-WhatIf</span></span>
<span data-ttu-id="218b6-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="218b6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="218b6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="218b6-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="218b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218b6-128">CommonParameters</span></span>
<span data-ttu-id="218b6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218b6-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="218b6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218b6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="218b6-131">INPUTS</span></span>

### <span data-ttu-id="218b6-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="218b6-132">None</span></span>
<span data-ttu-id="218b6-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="218b6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="218b6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="218b6-134">OUTPUTS</span></span>

### <span data-ttu-id="218b6-135">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="218b6-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="218b6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="218b6-136">NOTES</span></span>

## <span data-ttu-id="218b6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="218b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="218b6-138">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="218b6-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


