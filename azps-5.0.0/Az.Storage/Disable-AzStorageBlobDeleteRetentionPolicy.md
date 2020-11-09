---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281686"
---
# <span data-ttu-id="c965e-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c965e-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c965e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c965e-102">SYNOPSIS</span></span>
<span data-ttu-id="c965e-103">Desabilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c965e-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c965e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c965e-104">SYNTAX</span></span>

### <span data-ttu-id="c965e-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c965e-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c965e-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="c965e-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c965e-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c965e-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c965e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c965e-108">DESCRIPTION</span></span>
<span data-ttu-id="c965e-109">O cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c965e-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c965e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c965e-110">EXAMPLES</span></span>

### <span data-ttu-id="c965e-111">Exemplo 1: desabilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="c965e-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="c965e-112">Este comando desabilita a política de retenção de exclusão do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c965e-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="c965e-113">OS</span><span class="sxs-lookup"><span data-stu-id="c965e-113">PARAMETERS</span></span>

### <span data-ttu-id="c965e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c965e-114">-DefaultProfile</span></span>
<span data-ttu-id="c965e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c965e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c965e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c965e-116">-PassThru</span></span>
<span data-ttu-id="c965e-117">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="c965e-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="c965e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c965e-118">-ResourceGroupName</span></span>
<span data-ttu-id="c965e-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c965e-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c965e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c965e-120">-ResourceId</span></span>
<span data-ttu-id="c965e-121">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c965e-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c965e-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c965e-122">-StorageAccount</span></span>
<span data-ttu-id="c965e-123">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c965e-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c965e-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c965e-124">-StorageAccountName</span></span>
<span data-ttu-id="c965e-125">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c965e-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c965e-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c965e-126">-Confirm</span></span>
<span data-ttu-id="c965e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c965e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c965e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c965e-128">-WhatIf</span></span>
<span data-ttu-id="c965e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c965e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c965e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c965e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c965e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c965e-131">CommonParameters</span></span>
<span data-ttu-id="c965e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c965e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c965e-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c965e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c965e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c965e-134">INPUTS</span></span>

### <span data-ttu-id="c965e-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c965e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c965e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c965e-136">System.String</span></span>

## <span data-ttu-id="c965e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c965e-137">OUTPUTS</span></span>

### <span data-ttu-id="c965e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c965e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="c965e-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c965e-139">NOTES</span></span>

## <span data-ttu-id="c965e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c965e-140">RELATED LINKS</span></span>
