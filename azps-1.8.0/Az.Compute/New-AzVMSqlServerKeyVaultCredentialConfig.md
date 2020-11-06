---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: ec67022ff40247deb7d1ebc7e28bf7e1654fbd99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601300"
---
# <span data-ttu-id="d6714-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="d6714-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="d6714-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6714-102">SYNOPSIS</span></span>
<span data-ttu-id="d6714-103">Cria um objeto de configuração para a credencial do cofre de chaves do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d6714-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="d6714-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6714-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6714-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6714-105">DESCRIPTION</span></span>

## <span data-ttu-id="d6714-106">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6714-106">EXAMPLES</span></span>

## <span data-ttu-id="d6714-107">OS</span><span class="sxs-lookup"><span data-stu-id="d6714-107">PARAMETERS</span></span>

### <span data-ttu-id="d6714-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="d6714-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="d6714-109">URL do serviço do cofre de chaves do Azure</span><span class="sxs-lookup"><span data-stu-id="d6714-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="d6714-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d6714-110">-CredentialName</span></span>
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

### <span data-ttu-id="d6714-111">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="d6714-111">-Enable</span></span>
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

### <span data-ttu-id="d6714-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6714-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d6714-113">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="d6714-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="d6714-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="d6714-114">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="d6714-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6714-115">-Confirm</span></span>
<span data-ttu-id="d6714-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6714-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6714-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6714-117">-WhatIf</span></span>
<span data-ttu-id="d6714-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6714-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6714-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6714-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6714-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6714-120">CommonParameters</span></span>
<span data-ttu-id="d6714-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6714-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6714-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6714-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6714-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6714-123">INPUTS</span></span>

### <span data-ttu-id="d6714-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d6714-124">System.String</span></span>

### <span data-ttu-id="d6714-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6714-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d6714-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d6714-126">System.Security.SecureString</span></span>

## <span data-ttu-id="d6714-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6714-127">OUTPUTS</span></span>

### <span data-ttu-id="d6714-128">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d6714-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="d6714-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6714-129">NOTES</span></span>

## <span data-ttu-id="d6714-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6714-130">RELATED LINKS</span></span>
