---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428944"
---
# <span data-ttu-id="0a312-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="0a312-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="0a312-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a312-102">SYNOPSIS</span></span>
<span data-ttu-id="0a312-103">Tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a312-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a312-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a312-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a312-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a312-105">DESCRIPTION</span></span>
<span data-ttu-id="0a312-106">O cmdlet **Enable-AzureRmDataLakeStoreKeyVault** tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a312-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="0a312-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a312-107">EXAMPLES</span></span>

### <span data-ttu-id="0a312-108">Exemplo 1: habilitar o cofre de chaves para a conta do ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="0a312-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="0a312-109">Esse comando tenta habilitar o cofre de chave gerenciado pelo usuário para a conta do data Lake Store chamada ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="0a312-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="0a312-110">OS</span><span class="sxs-lookup"><span data-stu-id="0a312-110">PARAMETERS</span></span>

### <span data-ttu-id="0a312-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="0a312-111">-Account</span></span>
<span data-ttu-id="0a312-112">A conta do data Lake Store para habilitar o cofre de chave gerenciado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="0a312-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a312-113">-DefaultProfile</span></span>
<span data-ttu-id="0a312-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0a312-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a312-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a312-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a312-116">Nome do grupo de recursos associado à conta.</span><span class="sxs-lookup"><span data-stu-id="0a312-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="0a312-117">Se não for especificado, haverá uma tentativa de descoberta.</span><span class="sxs-lookup"><span data-stu-id="0a312-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a312-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a312-118">-Confirm</span></span>
<span data-ttu-id="0a312-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a312-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a312-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a312-120">-WhatIf</span></span>
<span data-ttu-id="0a312-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a312-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a312-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a312-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a312-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a312-123">CommonParameters</span></span>
<span data-ttu-id="0a312-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a312-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a312-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a312-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a312-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a312-126">INPUTS</span></span>

### <span data-ttu-id="0a312-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0a312-127">System.String</span></span>

## <span data-ttu-id="0a312-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a312-128">OUTPUTS</span></span>

## <span data-ttu-id="0a312-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a312-129">NOTES</span></span>

## <span data-ttu-id="0a312-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a312-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a312-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0a312-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0a312-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0a312-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

