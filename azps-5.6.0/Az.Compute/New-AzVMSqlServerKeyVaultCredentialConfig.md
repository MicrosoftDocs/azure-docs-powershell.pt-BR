---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 30bdfc03efd59b53cfed17b426b2b2411fb76d86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892538"
---
# <span data-ttu-id="d3fb5-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="d3fb5-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="d3fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fb5-103">Cria um objeto de configuração para SQL do cofre de chaves do servidor em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d3fb5-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="d3fb5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d3fb5-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3fb5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d3fb5-105">DESCRIPTION</span></span>

## <span data-ttu-id="d3fb5-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-106">EXAMPLES</span></span>

## <span data-ttu-id="d3fb5-107">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-107">PARAMETERS</span></span>

### <span data-ttu-id="d3fb5-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="d3fb5-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="d3fb5-109">URL de serviço do Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d3fb5-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="d3fb5-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d3fb5-110">-CredentialName</span></span>
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

### <span data-ttu-id="d3fb5-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="d3fb5-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fb5-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3fb5-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fb5-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d3fb5-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="d3fb5-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="d3fb5-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fb5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3fb5-115">-Confirm</span></span>
<span data-ttu-id="d3fb5-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3fb5-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fb5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3fb5-117">-WhatIf</span></span>
<span data-ttu-id="d3fb5-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3fb5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3fb5-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3fb5-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3fb5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fb5-120">CommonParameters</span></span>
<span data-ttu-id="d3fb5-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fb5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fb5-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3fb5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fb5-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-123">INPUTS</span></span>

### <span data-ttu-id="d3fb5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d3fb5-124">System.String</span></span>

### <span data-ttu-id="d3fb5-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3fb5-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d3fb5-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d3fb5-126">System.Security.SecureString</span></span>

## <span data-ttu-id="d3fb5-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-127">OUTPUTS</span></span>

### <span data-ttu-id="d3fb5-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d3fb5-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="d3fb5-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="d3fb5-129">NOTES</span></span>

## <span data-ttu-id="d3fb5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3fb5-130">RELATED LINKS</span></span>
