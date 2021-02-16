---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127037"
---
# <span data-ttu-id="be19b-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="be19b-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="be19b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be19b-102">SYNOPSIS</span></span>
<span data-ttu-id="be19b-103">Tenta habilitar um Cofre de Chave gerenciado pelo usuário para criptografia da conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="be19b-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="be19b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be19b-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be19b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="be19b-105">DESCRIPTION</span></span>
<span data-ttu-id="be19b-106">O cmdlet **Enable-AzDataLakeStoreKeyVault** tenta habilitar um Cofre de Chave gerenciado pelo usuário para criptografia da conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="be19b-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="be19b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be19b-107">EXAMPLES</span></span>

### <span data-ttu-id="be19b-108">Exemplo 1: Habilitar o Cofre de Teclas para a conta contosoADLS</span><span class="sxs-lookup"><span data-stu-id="be19b-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="be19b-109">Esse comando tenta habilitar o Cofre de Teclas gerenciado pelo usuário para a conta do Data Lake Store chamada ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="be19b-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="be19b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be19b-110">PARAMETERS</span></span>

### <span data-ttu-id="be19b-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="be19b-111">-Account</span></span>
<span data-ttu-id="be19b-112">A conta do Data Lake Store para habilitar o Cofre de Teclas gerenciado pelo usuário para</span><span class="sxs-lookup"><span data-stu-id="be19b-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="be19b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be19b-113">-DefaultProfile</span></span>
<span data-ttu-id="be19b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be19b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be19b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be19b-115">-ResourceGroupName</span></span>
<span data-ttu-id="be19b-116">Nome do grupo de recursos associado à conta.</span><span class="sxs-lookup"><span data-stu-id="be19b-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="be19b-117">Se não especificado, tentará ser descoberto.</span><span class="sxs-lookup"><span data-stu-id="be19b-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="be19b-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="be19b-118">-Confirm</span></span>
<span data-ttu-id="be19b-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be19b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be19b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be19b-120">-WhatIf</span></span>
<span data-ttu-id="be19b-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="be19b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be19b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be19b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be19b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be19b-123">CommonParameters</span></span>
<span data-ttu-id="be19b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be19b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be19b-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be19b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be19b-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="be19b-126">INPUTS</span></span>

### <span data-ttu-id="be19b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="be19b-127">System.String</span></span>

## <span data-ttu-id="be19b-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="be19b-128">OUTPUTS</span></span>

### <span data-ttu-id="be19b-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="be19b-129">System.Void</span></span>

## <span data-ttu-id="be19b-130">Notas</span><span class="sxs-lookup"><span data-stu-id="be19b-130">NOTES</span></span>

## <span data-ttu-id="be19b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be19b-131">RELATED LINKS</span></span>

[<span data-ttu-id="be19b-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="be19b-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="be19b-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="be19b-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

