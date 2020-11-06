---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440117"
---
# <span data-ttu-id="2ff63-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="2ff63-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="2ff63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ff63-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff63-103">Altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="2ff63-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ff63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ff63-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ff63-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ff63-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff63-106">O cmdlet **set-AzureBatchPoolOSVersion** altera a versão do sistema operacional do pool especificado.</span><span class="sxs-lookup"><span data-stu-id="2ff63-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="2ff63-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ff63-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff63-108">Exemplo 1: definir a versão do sistema operacional de destino de um pool</span><span class="sxs-lookup"><span data-stu-id="2ff63-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="2ff63-109">Esse comando define a versão do sistema operacional de destino do pool mypool como WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="2ff63-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="2ff63-110">OS</span><span class="sxs-lookup"><span data-stu-id="2ff63-110">PARAMETERS</span></span>

### <span data-ttu-id="2ff63-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2ff63-111">-BatchContext</span></span>
<span data-ttu-id="2ff63-112">Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="2ff63-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2ff63-113">Se você usar o cmdlet Get-AzureRmBatchAccount para obter o BatchAccountContext, a autenticação do Azure Active Directory será usada ao interagir com o serviço em lotes.</span><span class="sxs-lookup"><span data-stu-id="2ff63-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2ff63-114">Para usar a autenticação de chave compartilhada em vez disso, use o cmdlet Get-AzureRmBatchAccountKeys para obter um objeto BatchAccountContext com as teclas de acesso preenchidas.</span><span class="sxs-lookup"><span data-stu-id="2ff63-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2ff63-115">Ao usar a autenticação de chave compartilhada, a chave de acesso principal é usada por padrão.</span><span class="sxs-lookup"><span data-stu-id="2ff63-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2ff63-116">Para alterar a chave a ser usada, defina a propriedade BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2ff63-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff63-117">-DefaultProfile</span></span>
<span data-ttu-id="2ff63-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff63-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ff63-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2ff63-119">-Id</span></span>
<span data-ttu-id="2ff63-120">Especifica a ID do pool.</span><span class="sxs-lookup"><span data-stu-id="2ff63-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff63-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="2ff63-121">-TargetOSVersion</span></span>
<span data-ttu-id="2ff63-122">Especifica a versão do sistema operacional do Azure Guest a ser instalada nas máquinas virtuais do pool.</span><span class="sxs-lookup"><span data-stu-id="2ff63-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="2ff63-123">Para obter mais informações sobre as versões do sistema operacional convidado do Azure, consulte versões do sistema operacional do Azure Guest e matriz de compatibilidade do SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="2ff63-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff63-124">CommonParameters</span></span>
<span data-ttu-id="2ff63-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff63-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff63-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ff63-127">INPUTS</span></span>

### <span data-ttu-id="2ff63-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2ff63-128">BatchAccountContext</span></span>
<span data-ttu-id="2ff63-129">O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2ff63-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2ff63-130">String</span><span class="sxs-lookup"><span data-stu-id="2ff63-130">String</span></span>
<span data-ttu-id="2ff63-131">O parâmetro ' ID ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2ff63-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2ff63-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ff63-132">OUTPUTS</span></span>

## <span data-ttu-id="2ff63-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ff63-133">NOTES</span></span>

## <span data-ttu-id="2ff63-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ff63-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ff63-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2ff63-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


