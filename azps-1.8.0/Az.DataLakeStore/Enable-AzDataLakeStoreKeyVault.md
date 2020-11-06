---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 0e8adfc9ef5cfd5525a0e07b35c3eb1b918b9ba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601078"
---
# <span data-ttu-id="20b2b-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="20b2b-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="20b2b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="20b2b-103">Tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20b2b-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="20b2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20b2b-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b2b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="20b2b-106">O cmdlet **Enable-AzDataLakeStoreKeyVault** tenta habilitar um cofre de chaves gerenciados pelo usuário para a criptografia da conta especificada do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20b2b-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="20b2b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="20b2b-108">Exemplo 1: habilitar o cofre de chaves para a conta do ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="20b2b-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="20b2b-109">Esse comando tenta habilitar o cofre de chave gerenciado pelo usuário para a conta do data Lake Store chamada ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="20b2b-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="20b2b-110">OS</span><span class="sxs-lookup"><span data-stu-id="20b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="20b2b-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="20b2b-111">-Account</span></span>
<span data-ttu-id="20b2b-112">A conta do data Lake Store para habilitar o cofre de chave gerenciado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="20b2b-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="20b2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b2b-113">-DefaultProfile</span></span>
<span data-ttu-id="20b2b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="20b2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20b2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="20b2b-116">Nome do grupo de recursos associado à conta.</span><span class="sxs-lookup"><span data-stu-id="20b2b-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="20b2b-117">Se não for especificado, haverá uma tentativa de descoberta.</span><span class="sxs-lookup"><span data-stu-id="20b2b-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="20b2b-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20b2b-118">-Confirm</span></span>
<span data-ttu-id="20b2b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b2b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b2b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b2b-120">-WhatIf</span></span>
<span data-ttu-id="20b2b-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20b2b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20b2b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20b2b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b2b-123">CommonParameters</span></span>
<span data-ttu-id="20b2b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b2b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20b2b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b2b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20b2b-126">INPUTS</span></span>

### <span data-ttu-id="20b2b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="20b2b-127">System.String</span></span>

## <span data-ttu-id="20b2b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20b2b-128">OUTPUTS</span></span>

### <span data-ttu-id="20b2b-129">System. void</span><span class="sxs-lookup"><span data-stu-id="20b2b-129">System.Void</span></span>

## <span data-ttu-id="20b2b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20b2b-130">NOTES</span></span>

## <span data-ttu-id="20b2b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20b2b-131">RELATED LINKS</span></span>

[<span data-ttu-id="20b2b-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="20b2b-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="20b2b-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="20b2b-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

