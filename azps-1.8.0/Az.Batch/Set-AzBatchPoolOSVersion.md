---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93784983"
---
# <span data-ttu-id="daa20-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="daa20-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="daa20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daa20-102">SYNOPSIS</span></span>
<span data-ttu-id="daa20-103">Altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="daa20-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="daa20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daa20-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa20-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daa20-105">DESCRIPTION</span></span>
<span data-ttu-id="daa20-106">O cmdlet **set-AzBatchPoolOSVersion** altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="daa20-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="daa20-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daa20-107">EXAMPLES</span></span>

### <span data-ttu-id="daa20-108">Exemplo 1: definir a versão do sistema operacional de destino de um pool</span><span class="sxs-lookup"><span data-stu-id="daa20-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="daa20-109">Esse comando define a versão do sistema operacional de destino do pool mypool como WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="daa20-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="daa20-110">OS</span><span class="sxs-lookup"><span data-stu-id="daa20-110">PARAMETERS</span></span>

### <span data-ttu-id="daa20-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="daa20-111">-BatchContext</span></span>
<span data-ttu-id="daa20-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="daa20-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="daa20-113">Se você usar o cmdlet Get-AzBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="daa20-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="daa20-114">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="daa20-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="daa20-115">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="daa20-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="daa20-116">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="daa20-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daa20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa20-117">-DefaultProfile</span></span>
<span data-ttu-id="daa20-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daa20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa20-119">-ID</span><span class="sxs-lookup"><span data-stu-id="daa20-119">-Id</span></span>
<span data-ttu-id="daa20-120">Especifica a ID do pool.</span><span class="sxs-lookup"><span data-stu-id="daa20-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daa20-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="daa20-121">-TargetOSVersion</span></span>
<span data-ttu-id="daa20-122">Especifica a versão do sistema operacional do Azure Guest a ser instalada nas máquinas virtuais do pool.</span><span class="sxs-lookup"><span data-stu-id="daa20-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="daa20-123">Para obter mais informações sobre as versões do sistema operacional convidado do Azure, consulte versões do sistema operacional do Azure Guest e matriz de compatibilidade do SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="daa20-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa20-124">CommonParameters</span></span>
<span data-ttu-id="daa20-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa20-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa20-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daa20-127">INPUTS</span></span>

### <span data-ttu-id="daa20-128">System. String</span><span class="sxs-lookup"><span data-stu-id="daa20-128">System.String</span></span>

### <span data-ttu-id="daa20-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="daa20-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="daa20-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daa20-130">OUTPUTS</span></span>

### <span data-ttu-id="daa20-131">System. void</span><span class="sxs-lookup"><span data-stu-id="daa20-131">System.Void</span></span>

## <span data-ttu-id="daa20-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daa20-132">NOTES</span></span>

## <span data-ttu-id="daa20-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daa20-133">RELATED LINKS</span></span>

[<span data-ttu-id="daa20-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="daa20-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


