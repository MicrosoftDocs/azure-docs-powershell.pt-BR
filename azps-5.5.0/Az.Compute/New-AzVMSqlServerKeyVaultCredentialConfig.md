---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112108"
---
# <span data-ttu-id="fd241-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="fd241-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="fd241-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd241-102">SYNOPSIS</span></span>
<span data-ttu-id="fd241-103">Cria um objeto de configuração para a credencial do cofre de teclas do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fd241-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="fd241-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd241-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd241-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd241-105">DESCRIPTION</span></span>

## <span data-ttu-id="fd241-106">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd241-106">EXAMPLES</span></span>

## <span data-ttu-id="fd241-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd241-107">PARAMETERS</span></span>

### <span data-ttu-id="fd241-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="fd241-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="fd241-109">URL de serviço do Cofre de Chave do Azure</span><span class="sxs-lookup"><span data-stu-id="fd241-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="fd241-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fd241-110">-CredentialName</span></span>
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

### <span data-ttu-id="fd241-111">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="fd241-111">-Enable</span></span>
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

### <span data-ttu-id="fd241-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd241-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fd241-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd241-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="fd241-114">-ServicePrincipalSec limited</span><span class="sxs-lookup"><span data-stu-id="fd241-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="fd241-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fd241-115">-Confirm</span></span>
<span data-ttu-id="fd241-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd241-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd241-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd241-117">-WhatIf</span></span>
<span data-ttu-id="fd241-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fd241-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd241-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd241-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd241-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd241-120">CommonParameters</span></span>
<span data-ttu-id="fd241-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd241-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd241-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd241-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd241-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd241-123">INPUTS</span></span>

### <span data-ttu-id="fd241-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fd241-124">System.String</span></span>

### <span data-ttu-id="fd241-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fd241-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fd241-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="fd241-126">System.Security.SecureString</span></span>

## <span data-ttu-id="fd241-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd241-127">OUTPUTS</span></span>

### <span data-ttu-id="fd241-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="fd241-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="fd241-129">Notas</span><span class="sxs-lookup"><span data-stu-id="fd241-129">NOTES</span></span>

## <span data-ttu-id="fd241-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd241-130">RELATED LINKS</span></span>
