---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 2b4b225ca050e3efedb1de1371006a4ffdb87587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885470"
---
# <span data-ttu-id="60fbc-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="60fbc-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="60fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="60fbc-103">Tenta habilitar um Cofre de Chaves gerenciado pelo usuário para criptografia da conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="60fbc-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="60fbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="60fbc-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60fbc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="60fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="60fbc-106">O cmdlet **Enable-AzDataLakeStoreKeyVault** tenta habilitar um Cofre de Chaves gerenciado pelo usuário para criptografia da conta especificada do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="60fbc-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="60fbc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="60fbc-108">Exemplo 1: Habilitar o Cofre de Chaves para a conta ContosoADLS</span><span class="sxs-lookup"><span data-stu-id="60fbc-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="60fbc-109">Este comando tenta habilitar o Cofre de Chaves gerenciado pelo usuário para a conta do Data Lake Store chamada ContosoADLS.</span><span class="sxs-lookup"><span data-stu-id="60fbc-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="60fbc-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="60fbc-110">PARAMETERS</span></span>

### <span data-ttu-id="60fbc-111">-Account</span><span class="sxs-lookup"><span data-stu-id="60fbc-111">-Account</span></span>
<span data-ttu-id="60fbc-112">A conta do Data Lake Store para habilitar o Cofre de Chaves gerenciado pelo usuário para</span><span class="sxs-lookup"><span data-stu-id="60fbc-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="60fbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fbc-113">-DefaultProfile</span></span>
<span data-ttu-id="60fbc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="60fbc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60fbc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fbc-115">-ResourceGroupName</span></span>
<span data-ttu-id="60fbc-116">Nome do grupo de recursos associado à conta.</span><span class="sxs-lookup"><span data-stu-id="60fbc-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="60fbc-117">Se não especificado, tentará ser descoberto.</span><span class="sxs-lookup"><span data-stu-id="60fbc-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="60fbc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60fbc-118">-Confirm</span></span>
<span data-ttu-id="60fbc-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60fbc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60fbc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60fbc-120">-WhatIf</span></span>
<span data-ttu-id="60fbc-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60fbc-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60fbc-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60fbc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60fbc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fbc-123">CommonParameters</span></span>
<span data-ttu-id="60fbc-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fbc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fbc-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fbc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fbc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60fbc-126">INPUTS</span></span>

### <span data-ttu-id="60fbc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="60fbc-127">System.String</span></span>

## <span data-ttu-id="60fbc-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="60fbc-128">OUTPUTS</span></span>

### <span data-ttu-id="60fbc-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="60fbc-129">System.Void</span></span>

## <span data-ttu-id="60fbc-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="60fbc-130">NOTES</span></span>

## <span data-ttu-id="60fbc-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60fbc-131">RELATED LINKS</span></span>

[<span data-ttu-id="60fbc-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="60fbc-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="60fbc-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="60fbc-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

