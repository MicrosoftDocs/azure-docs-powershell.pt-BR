---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948455"
---
# <span data-ttu-id="1ed14-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="1ed14-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="1ed14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ed14-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed14-103">Adiciona um ouvinte WinRM ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed14-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="1ed14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ed14-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ed14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ed14-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed14-106">O cmdlet **Add-AzVmssWinRMListener** adiciona um ouvinte do Windows Remote Management (WinRM) no conjunto de escala da máquina virtual (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1ed14-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1ed14-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ed14-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed14-108">Exemplo 1: adicionar um ouvinte do WinRM ao VMSS</span><span class="sxs-lookup"><span data-stu-id="1ed14-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="1ed14-109">Este exemplo adiciona um ouvinte do WinRM ao VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed14-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="1ed14-110">O primeiro comando usa o cmdlet **New-AzVmssConfig** para criar um objeto de configuração VMSS e armazena o resultado na variável chamada $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed14-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="1ed14-111">O segundo comando adiciona um ouvinte de protocolo HTTP WinRM com o certificado na URL especificada para o VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed14-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="1ed14-112">OS</span><span class="sxs-lookup"><span data-stu-id="1ed14-112">PARAMETERS</span></span>

### <span data-ttu-id="1ed14-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1ed14-113">-CertificateUrl</span></span>
<span data-ttu-id="1ed14-114">Especifica um link, como uma URL, do certificado com o qual novas máquinas virtuais são provisionadas.</span><span class="sxs-lookup"><span data-stu-id="1ed14-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed14-115">-DefaultProfile</span></span>
<span data-ttu-id="1ed14-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed14-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ed14-117">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="1ed14-117">-Protocol</span></span>
<span data-ttu-id="1ed14-118">Especifica o protocolo do ouvinte de WinRM.</span><span class="sxs-lookup"><span data-stu-id="1ed14-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="1ed14-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="1ed14-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ed14-120">Http</span><span class="sxs-lookup"><span data-stu-id="1ed14-120">Http</span></span>
- <span data-ttu-id="1ed14-121">Https</span><span class="sxs-lookup"><span data-stu-id="1ed14-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed14-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ed14-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1ed14-123">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed14-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="1ed14-124">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1ed14-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed14-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ed14-125">-Confirm</span></span>
<span data-ttu-id="1ed14-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed14-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed14-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed14-127">-WhatIf</span></span>
<span data-ttu-id="1ed14-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ed14-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ed14-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ed14-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed14-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed14-130">CommonParameters</span></span>
<span data-ttu-id="1ed14-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed14-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed14-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ed14-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed14-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ed14-133">INPUTS</span></span>

### <span data-ttu-id="1ed14-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ed14-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1ed14-135">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. ProtocolTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1ed14-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1ed14-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1ed14-136">System.String</span></span>

## <span data-ttu-id="1ed14-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ed14-137">OUTPUTS</span></span>

### <span data-ttu-id="1ed14-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ed14-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1ed14-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ed14-139">NOTES</span></span>

## <span data-ttu-id="1ed14-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ed14-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ed14-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1ed14-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


