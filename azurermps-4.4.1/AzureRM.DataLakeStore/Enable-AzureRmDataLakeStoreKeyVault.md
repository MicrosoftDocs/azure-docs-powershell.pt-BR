---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: a168b48089052ed8daa764407254d04084ece771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427944"
---
# <span data-ttu-id="2faf9-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="2faf9-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="2faf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2faf9-102">SYNOPSIS</span></span>
<span data-ttu-id="2faf9-103">Tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2faf9-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2faf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2faf9-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2faf9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2faf9-105">DESCRIPTION</span></span>
<span data-ttu-id="2faf9-106">O cmdlet **Enable-AzureRmDataLakeStoreKeyVault** tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2faf9-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="2faf9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2faf9-107">EXAMPLES</span></span>

### <span data-ttu-id="2faf9-108">Exemplo 1: habilitar o cofre de chaves para a conta do ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="2faf9-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="2faf9-109">Esse comando tenta habilitar o cofre de chave gerenciado pelo usuário para a conta do data Lake Store chamada ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="2faf9-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="2faf9-110">OS</span><span class="sxs-lookup"><span data-stu-id="2faf9-110">PARAMETERS</span></span>

### <span data-ttu-id="2faf9-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2faf9-111">-Account</span></span>
<span data-ttu-id="2faf9-112">A conta do data Lake Store para habilitar o cofre de chave gerenciado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="2faf9-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2faf9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faf9-113">-ResourceGroupName</span></span>
<span data-ttu-id="2faf9-114">Nome do grupo de recursos associado à conta.</span><span class="sxs-lookup"><span data-stu-id="2faf9-114">Name of resource group associated with the account.</span></span> <span data-ttu-id="2faf9-115">Se não for especificado, haverá uma tentativa de descoberta.</span><span class="sxs-lookup"><span data-stu-id="2faf9-115">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2faf9-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2faf9-116">-Confirm</span></span>
<span data-ttu-id="2faf9-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2faf9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2faf9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2faf9-118">-WhatIf</span></span>
<span data-ttu-id="2faf9-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2faf9-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2faf9-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2faf9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2faf9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2faf9-121">-DefaultProfile</span></span>
<span data-ttu-id="2faf9-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2faf9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2faf9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2faf9-123">CommonParameters</span></span>
<span data-ttu-id="2faf9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2faf9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2faf9-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2faf9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2faf9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2faf9-126">INPUTS</span></span>

### <span data-ttu-id="2faf9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2faf9-127">System.String</span></span>

## <span data-ttu-id="2faf9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2faf9-128">OUTPUTS</span></span>

## <span data-ttu-id="2faf9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2faf9-129">NOTES</span></span>

## <span data-ttu-id="2faf9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2faf9-130">RELATED LINKS</span></span>

[<span data-ttu-id="2faf9-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2faf9-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="2faf9-132">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="2faf9-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

