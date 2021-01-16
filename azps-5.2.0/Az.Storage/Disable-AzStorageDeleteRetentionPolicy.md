---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: c8a32cb86ace86cb0f2775db98f49f57408be6f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261013"
---
# <span data-ttu-id="44c48-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="44c48-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="44c48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44c48-102">SYNOPSIS</span></span>
<span data-ttu-id="44c48-103">Desabilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44c48-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="44c48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44c48-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44c48-105">DESCRIPTION</span></span>
<span data-ttu-id="44c48-106">O cmdlet **Disable-AzStorageDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44c48-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="44c48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44c48-107">EXAMPLES</span></span>

### <span data-ttu-id="44c48-108">Exemplo 1: desabilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="44c48-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="44c48-109">Este comando desabilita a política de retenção de exclusão do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="44c48-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="44c48-110">OS</span><span class="sxs-lookup"><span data-stu-id="44c48-110">PARAMETERS</span></span>

### <span data-ttu-id="44c48-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="44c48-111">-Context</span></span>
<span data-ttu-id="44c48-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="44c48-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44c48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c48-113">-DefaultProfile</span></span>
<span data-ttu-id="44c48-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44c48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44c48-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44c48-115">-PassThru</span></span>
<span data-ttu-id="44c48-116">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="44c48-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="44c48-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44c48-117">-Confirm</span></span>
<span data-ttu-id="44c48-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c48-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c48-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c48-119">-WhatIf</span></span>
<span data-ttu-id="44c48-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44c48-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c48-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44c48-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c48-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c48-122">CommonParameters</span></span>
<span data-ttu-id="44c48-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c48-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c48-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c48-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c48-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44c48-125">INPUTS</span></span>

### <span data-ttu-id="44c48-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="44c48-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="44c48-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44c48-127">OUTPUTS</span></span>

### <span data-ttu-id="44c48-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="44c48-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="44c48-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44c48-129">NOTES</span></span>

## <span data-ttu-id="44c48-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44c48-130">RELATED LINKS</span></span>
